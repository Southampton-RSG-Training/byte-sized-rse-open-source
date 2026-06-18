---
title: "Contributing to Open Source"
teaching: 15
exercises: 0
---

:::::::::::::::::::::::::::::::::::::: questions 

- Should I contribute to an open source project?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- ...

::::::::::::::::::::::::::::::::::::::::::::::::

# Activity

In this activity we'll work through the steps needed to make a pull request against a third-party open source project.

## Example Repository

The instructor will give you a link to the code repository you will be working with.

Rather than a code, this repository contains information about the folk tale "Stone Soup":

``` markdown
# Stone Soup

The folk story [Stone Soup](https://en.wikipedia.org/wiki/Stone_Soup) is an excellend allegory for the way that open source software can work.  From Wikipedia:

> Some travelers come to a village, carrying nothing more than an empty cooking pot. Upon their arrival, the villagers are unwilling to share any of their food stores with the very hungry travelers. Then the travelers go to a stream and fill the pot with water, drop a large stone in it, and place it over a fire. One of the villagers becomes curious and asks what they are doing. The travelers answer that they are making "stone soup", which tastes wonderful and which they would be delighted to share with the villager, although it still needs a little bit of garnish, which they are missing, to improve the flavor.
> 
> The villager, who anticipates enjoying a share of the soup, does not mind parting with a few carrots, so these are added to the soup. Another villager walks by, inquiring about the pot, and the travelers again mention their stone soup which has not yet reached its full potential. More and more villagers walk by, each adding another ingredient, like potatoes, onions, cabbages, peas, celery, tomatoes, sweetcorn, meat (like chicken, pork and beef), milk, butter, salt and pepper. Finally, the stone (being inedible) is removed from the pot, and a delicious and nourishing pot of soup is enjoyed by travelers and villagers alike. Although the travelers have thus tricked the villagers into sharing their food with them, they have successfully transformed it into a tasty meal which they share with the donors.

## Recipe

Place a large pot of water over low heat and add:

- a stone

Simmer until done.  Remove stone and serve the soup.
```

Clearly, the recipe needs more ingredients.

### Open an Issue

Go to the GitHub repository and open an issue that suggests a way that the recipe can be improved: perhaps an ingredient to add?

### Fork the Repository

On the main page of the repository, click the "Fork" button.  You should see a page which allows you to change the name of the repository. Accept the default settings.

You should now have a copy of the GitHub repository in your GitHUb account.

### Clone the Repository

In the "Code" button on *your* fork of the repository, copy the URL. Change directory to your root directory and then paste it into a clone command in your shell:

``` bash
cd
git clone .../stone-soup-example
cd stone-soup-example
```

### Create a Branch and Make Your Changes

Choose an issue that you will work on and use git to create a branch for your work.  You might want to use your name in the branch name, or some other way of making sure it doesn't conflict with the names that other people choose for their work.

Now edit the recipe with your improvement or fixes and commit the changes.

### Push the Branch and Open a PR

Once you have made your updates, push the branch to your fork.

``` bash
git push origin ...
```

As usual, the message gives you a GitHub URL you can open to create the pull request, or you can go to your fork on github and find the branch there to open the pull request.  However, when you start to make the PR you will see that the target for your pull request will be the upstream repository.

Fill in the description of your pull request, and then go to the upstream repository and you should see your pull request.

### Resolving Merge Conflicts

After the first of the pull requests is merged, it is likely that your pull request can no longer be automatically merged.  In some projects the maintainer may manage the conflict resolution themselves, but you can also do it yourself.

Go to your fork and select the sync repository button.

In your local clone switch to the main branch and pull from your fork:
``` bash
git switch main
git pull
```

Then switch back to your branch and merge main (using a normal three-way merge, *don't* do a rebase merge), resolving any conflicts.
``` bash
git switch ...
git merge main
```

Then push your changes back to your fork:
``` bash
git push origin ...
```


