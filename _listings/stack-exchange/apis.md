---
name: Stack Exchange
x-slug: stack-exchange
description: After someone asks a question, members of the community propose answers.
  Others vote on those answers. Very quickly, the answers with the most votes rise
  to the top. You dont have to read through a lot of discussion to find the best answer.    Like
  to...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
x-kinRank: "8"
x-alexaRank: "126"
tags: Answers
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/apis.md
specificationVersion: "0.14"
apis:
- name: Stack Exchange Get Answers
  x-api-slug: stack-exchange
  description: "Returns all the undeleted answers in the system.\n \nThe sorts accepted
    by this method operate on the follow fields of the answer object:\n - activity
    - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    answers."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//answers
  tags: Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/answers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/answers-get-openapi.md
- name: Stack Exchange Get Answer
  x-api-slug: stack-exchange
  description: "Gets the set of answers identified by ids.\n \nThis is meant for batch
    fetcing of questions. A useful trick to poll for updates is to sort by activity,
    with a minimum date of the last time you polled.\n \n{ids} can contain up to 100
    semicolon delimited ids, to find ids programatically look for answer_id on answer
    objects.\n \nThe sorts accepted by this method operate on the follow fields of
    the answer object:\n - activity - last_activity_date\n - creation - creation_date\n
    - votes - score\n  activity is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//answers/{ids}
  tags: Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/answersids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/answersids-get-openapi.md
- name: Stack Exchange Get Answer Comments
  x-api-slug: stack-exchange
  description: "Gets the comments on a set of answers.\n \nIf you know that you have
    an answer id and need the comments, use this method. If you know you have a question
    id, use /questions/{id}/comments. If you are unsure, use /posts/{id}/comments.\n
    \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
    look for answer_id on answer objects.\n \nThe sorts accepted by this method operate
    on the follow fields of the comment object:\n - creation - creation_date\n - votes
    - score\n  creation is the default sort.\n \n It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//answers/{ids}/comments
  tags: Answers,comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/answersidscomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/answersidscomments-get-openapi.md
- name: Stack Exchange My Answers
  x-api-slug: stack-exchange
  description: "Returns the answers owned by the user associated with the given access_token.\n
    \nThis method returns a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//me/answers
  tags: Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/meanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/meanswers-get-openapi.md
- name: Stack Exchange Get Question Answers
  x-api-slug: stack-exchange
  description: "Gets the answers to a set of questions identified in id.\n \nThis
    method is most useful if you have a set of interesting questions, and you wish
    to obtain all of their answers at once or if you are polling for new or updates
    answers (in conjunction with sort=activity).\n \n{ids} can contain up to 100 semicolon
    delimited ids, to find ids programatically look for question_id on question objects.\n
    \nThe sorts accepted by this method operate on the follow fields of the answer
    object:\n - activity - last_activity_date\n - creation - creation_date\n - votes
    - score\n  activity is the default sort.\n \n It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//questions/{ids}/answers
  tags: Questions,Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/questionsidsanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/questionsidsanswers-get-openapi.md
- name: Stack Exchange Get Tags Top Answers
  x-api-slug: stack-exchange
  description: "Returns the top 30 answerers active in a single tag, of either all-time
    or the last 30 days.\n \nThis is a view onto the data presented on the tag info
    page on the sites.\n \nThis method returns a list of tag score objects."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//tags/{tag}/top-answerers/{period}
  tags: Tags,Top Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/tagstagtopanswerersperiod-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/tagstagtopanswerersperiod-get-openapi.md
- name: Stack Exchange Get User Answers
  x-api-slug: stack-exchange
  description: "Returns the answers the users in {ids} have posted.\n \n{ids} can
    contain up to 100 semicolon delimited ids, to find ids programatically look for
    user_id on user or shallow_user objects.\n \nThe sorts accepted by this method
    operate on the follow fields of the answer object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/answers
  tags: Users,Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/usersidsanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/usersidsanswers-get-openapi.md
- name: Stack Exchange Get User Questions No Answers
  x-api-slug: stack-exchange
  description: "Gets the questions asked by the users in {ids} which have no answers.\n
    \nQuestions returns by this method actually have zero undeleted answers. It is
    completely disjoint /users/{ids}/questions/unanswered and /users/{ids}/questions/unaccepted,
    which only return questions with at least one answer, subject to other contraints.\n
    \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
    look for user_id on user or shallow_user objects.\n \nThe sorts accepted by this
    method operate on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/questions/no-answers
  tags: Users,Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/usersidsquestionsnoanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/usersidsquestionsnoanswers-get-openapi.md
- name: Stack Exchange Get User Tags Top Answers
  x-api-slug: stack-exchange
  description: "Returns the top 30 answers a user has posted in response to questions
    with the given tags.\n \n{id} can contain a single id, to find it programatically
    look for user_id on user or shallow_user objects. {tags} is limited to 5 tags,
    passing more will result in an error.\n \nThe sorts accepted by this method operate
    on the follow fields of the answer object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//users/{id}/tags/{tags}/top-answers
  tags: Users,Tags,Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/usersidtagstagstopanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/usersidtagstagstopanswers-get-openapi.md
- name: Stack Exchange
  x-api-slug: stack-exchange
  description: After someone asks a question, members of the community propose answers.
    Others vote on those answers. Very quickly, the answers with the most votes rise
    to the top. You dont have to read through a lot of discussion to find the best
    answer.    Like to...
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Answers
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/answers/master/_listings/stack-exchange/openapi.md
x-common:
- type: x-authentication
  url: https://api.stackexchange.com/docs/authentication
- type: x-base
  url: https://api.stackexchange.com/
- type: x-blog
  url: http://stackexchange.com/blogs
- type: x-blog-rss
  url: http://blog.stackoverflow.com/feed/
- type: x-crunchbase
  url: http://www.crunchbase.com/company/stack-exchange
- type: x-crunchbase
  url: https://crunchbase.com/organization/stack-exchange
- type: x-developer
  url: http://api.stackexchange.com/
- type: x-email
  url: legal@stackexchange.com
- type: x-email
  url: team@stackexchange.com
- type: x-email
  url: team+api@stackexchange.com
- type: x-error-codes
  url: https://api.stackexchange.com/docs/error-handling
- type: x-github
  url: https://github.com/StackExchange
- type: x-javascript-sdk
  url: https://api.stackexchange.com/docs/js-lib
- type: x-linkedin
  url: https://www.linkedin.com/company/stack-exchange
- type: x-privacy
  url: https://stackexchange.com/legal/privacy-policy
- type: x-rate-limits
  url: https://api.stackexchange.com/docs/throttle
- type: x-selfservice-registration
  url: https://stackapps.com/users/login?returnurl=/apps/oauth/register
- type: x-support
  url: https://stackexchange.com/about/contact
- type: x-terms-of-service
  url: http://stackexchange.com/legal/api-terms-of-use
- type: x-twitter
  url: https://twitter.com/StackExchange
- type: x-website
  url: http://stackexchange.com
- type: x-website
  url: https://stackexchange.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---