#!/bin/bash

helper()

#GitHb API URL
API_URL = "https://api.github.com"

#GitHub Username and Personal Access Token
USERNAME = $username
TOKEN = $token

#User and Repository Information
REPO_OWNER = $1
REPO_NAME = $2

#Function to make a git request to the GitHub API
function github_api_get {
    local endpoint = "$1"
    local url = ${API_URL}/${endpoint}"

#Send a GET Request to the GitHub API with Authentication
curl -s -u "${USERNAME}:${TOKEN}" "$url"
}

#Function to list users with read access to the repository
function list_users_with_read_access{
    local endpoint = "repos/${REPO_OWNER}/${REPO_NAME}/collaborators"

    #Fetch the lit of collaboraters with read access
    if [[ -z "$collaborators"]]; then
        echo "no users with read access found for $REPO_OWNER/$REPO_NAME}."
    else
        echo "users with read access to ${REPO_OWNER/$REPO_NAME}."
        echo "$collaboraters"
    fi
}

#Main Script
echo "List users with read access to ${REPO_OWNER}/${REPO_NAME}"
list_users_with_read_access

#Helper function
function helper{
    expected_cmd_args=2
    if[$# -ne $expected_cmd_args];then
    echo "Please execute the script with required cmd args"
    echo "asd"
}
