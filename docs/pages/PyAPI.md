---
title: Python Call API
layout: default
excerpt: Place the introducing line of text ie.) the 'tagline' here ...
hint: Certainly! To search an API for a team nickname, you will need to send a request to the API and process the response to extract the desired information. Here's an example Python code snippet that demonstrates how you can accomplish this using the requests library ...
repo: Python-Lessons-Project
ver_date: 11-26-19
navigation_weight: 8
categories: template
---
{% include toc.md %}

## First Subtitle

> **Hint**. {{ page.hint }}

More to come ...

## Import Code

```html
<hgroup class='text-left'>
    <h4>Strict Objects</h4>
</hgroup>
    <hr class='green-groove' />

<p>
    <span>Now, that works fine.</span>
    <span>But, how will the code execute in Strict Mode?</span>
    <span>One way to find out is to transfer our code to a (<a href="../js/scripts/strict-objects.js" title="Click To Review the Original Javascript file" target="_blank">.js</a>) page and invoke Strict Mode at the top of the program.</span>
</p>

<pre class='flex-box'>
<span>Invoke Strict Mode ...</span>
{% highlight Python linenos %}
//Py API Call
import requests

def search_team_nickname(api_url, team_name):
    # Create the API request URL with the query parameter
    request_url = f"{api_url}?team_name={team_name}"

    # Send a GET request to the API
    response = requests.get(request_url)

    # Check if the request was successful (status code 200)
    if response.status_code == 200:
        # Parse the response JSON
        data = response.json()

        # Extract the team nickname from the response
        team_nickname = data["nickname"]

        return team_nickname

    # Request was not successful, return None
    return None
{% endhighlight %}
<span>Place at the top of program.</span>
</pre>
<hr class='green-groove' />

<p>
    <span>Let's try that.</span>
</p>

<p>
    <span>Copy and paste the contents of the entire (<a href='../js/scripts/strict-objects.js' title='Click To Review the Original Javascript file' target='_blank'>.js</a>) file into the Firefox Web-console ...</span>
    <span>Then, hit the <kbd>Enter</kbd> key.</span>
</p>

<pre class='flex-box'>
    <span lang='es' title='Sp. for 'Finish''>Finito! <i class='icon-large icon-flower'></i></span>
</pre>
```

## Example usage

api_url = "https://api.example.com/teams"  # Replace with the actual API URL
team_name = "Los Angeles Lakers"  # Replace with the team name you want to search for

nickname = search_team_nickname(api_url, team_name)
if nickname:
    print(f"The nickname of {team_name} is: {nickname}")
else:
    print(f"Unable to find the nickname for {team_name}.")

In this example, you need to replace "https://api.example.com/teams" with the actual URL of the API you want to use. Additionally, make sure the API endpoint supports searching for team nicknames using a query parameter like team_name.

## Last Subtitle

More to come ...

***

**Note**. The above synopsis was derived from an article written by Blank Author [[1](#BLANKAUTHOR){:.red}].

1. {:#BLANKAUTHOR}[A Narrative of Psychology by Blank Author, Jan #1999](http://cowles.yale.edu/sites/default/files/files/pub/d20/d2069.pdf){:title="Click to Review ..."}{:target="_blank"}

***

{% include patreon-link.md %}
