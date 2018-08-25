---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 0
info:
  title: Stack Exchange Get User Tags Top Answers
  description: "Returns the top 30 answers a user has posted in response to questions
    with the given tags.\n \n{id} can contain a single id, to find it programatically
    look for user_id on user or shallow_user objects. {tags} is limited to 5 tags,
    passing more will result in an error.\n \nThe sorts accepted by this method operate
    on the follow fields of the answer object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of answers."
  version: "2.0"
host: api.stackexchange.com
basePath: /2.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /answers:
    get:
      summary: Get Answers
      description: "Returns all the undeleted answers in the system.\n \nThe sorts
        accepted by this method operate on the follow fields of the answer object:\n
        - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
        \ activity is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate.\n \nThis method returns
        a list of answers."
      operationId: returns-all-the-undeleted-answers-in-the-system-the-sorts-accepted-by-this-method-operate-on-the-fol
      x-api-path-slug: answers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: Filter the discussion
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Answers
  /answers/{ids}:
    get:
      summary: Get Answer
      description: "Gets the set of answers identified by ids.\n \nThis is meant for
        batch fetcing of questions. A useful trick to poll for updates is to sort
        by activity, with a minimum date of the last time you polled.\n \n{ids} can
        contain up to 100 semicolon delimited ids, to find ids programatically look
        for answer_id on answer objects.\n \nThe sorts accepted by this method operate
        on the follow fields of the answer object:\n - activity - last_activity_date\n
        - creation - creation_date\n - votes - score\n  activity is the default sort.\n
        \n It is possible to create moderately complex queries using sort, min, max,
        fromdate, and todate.\n \nThis method returns a list of answers."
      operationId: gets-the-set-of-answers-identified-by-ids-this-is-meant-for-batch-fetcing-of-questions-a-useful-tric
      x-api-path-slug: answersids-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Answers
  /answers/{ids}/comments:
    get:
      summary: Get Answer Comments
      description: "Gets the comments on a set of answers.\n \nIf you know that you
        have an answer id and need the comments, use this method. If you know you
        have a question id, use /questions/{id}/comments. If you are unsure, use /posts/{id}/comments.\n
        \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
        look for answer_id on answer objects.\n \nThe sorts accepted by this method
        operate on the follow fields of the comment object:\n - creation - creation_date\n
        - votes - score\n  creation is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of comments."
      operationId: gets-the-comments-on-a-set-of-answers-if-you-know-that-you-have-an-answer-id-and-need-the-comments-u
      x-api-path-slug: answersidscomments-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Answers
      - comments
  /me/answers:
    get:
      summary: My Answers
      description: "Returns the answers owned by the user associated with the given
        access_token.\n \nThis method returns a list of answers."
      operationId: returns-the-answers-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-l
      x-api-path-slug: meanswers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Answers
  /questions/{ids}/answers:
    get:
      summary: Get Question Answers
      description: "Gets the answers to a set of questions identified in id.\n \nThis
        method is most useful if you have a set of interesting questions, and you
        wish to obtain all of their answers at once or if you are polling for new
        or updates answers (in conjunction with sort=activity).\n \n{ids} can contain
        up to 100 semicolon delimited ids, to find ids programatically look for question_id
        on question objects.\n \nThe sorts accepted by this method operate on the
        follow fields of the answer object:\n - activity - last_activity_date\n -
        creation - creation_date\n - votes - score\n  activity is the default sort.\n
        \n It is possible to create moderately complex queries using sort, min, max,
        fromdate, and todate.\n \nThis method returns a list of answers."
      operationId: gets-the-answers-to-a-set-of-questions-identified-in-id-this-method-is-most-useful-if-you-have-a-set
      x-api-path-slug: questionsidsanswers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Questions
      - Answers
  /users/{ids}/answers:
    get:
      summary: Get User Answers
      description: "Returns the answers the users in {ids} have posted.\n \n{ids}
        can contain up to 100 semicolon delimited ids, to find ids programatically
        look for user_id on user or shallow_user objects.\n \nThe sorts accepted by
        this method operate on the follow fields of the answer object:\n - activity
        - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of answers."
      operationId: returns-the-answers-the-users-in-ids-have-posted-ids-can-contain-up-to-100-semicolon-delimited-ids-t
      x-api-path-slug: usersidsanswers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Answers
  /users/{ids}/questions/no-answers:
    get:
      summary: Get User Questions No Answers
      description: "Gets the questions asked by the users in {ids} which have no answers.\n
        \nQuestions returns by this method actually have zero undeleted answers. It
        is completely disjoint /users/{ids}/questions/unanswered and /users/{ids}/questions/unaccepted,
        which only return questions with at least one answer, subject to other contraints.\n
        \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
        look for user_id on user or shallow_user objects.\n \nThe sorts accepted by
        this method operate on the follow fields of the question object:\n - activity
        - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of questions."
      operationId: gets-the-questions-asked-by-the-users-in-ids-which-have-no-answers-questions-returns-by-this-method-
      x-api-path-slug: usersidsquestionsnoanswers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Answers
  /users/{id}/tags/{tags}/top-answers:
    get:
      summary: Get User Tags Top Answers
      description: "Returns the top 30 answers a user has posted in response to questions
        with the given tags.\n \n{id} can contain a single id, to find it programatically
        look for user_id on user or shallow_user objects. {tags} is limited to 5 tags,
        passing more will result in an error.\n \nThe sorts accepted by this method
        operate on the follow fields of the answer object:\n - activity - last_activity_date\n
        - creation - creation_date\n - votes - score\n  activity is the default sort.\n
        \n It is possible to create moderately complex queries using sort, min, max,
        fromdate, and todate.\n \nThis method returns a list of answers."
      operationId: returns-the-top-30-answers-a-user-has-posted-in-response-to-questions-with-the-given-tags-id-can-con
      x-api-path-slug: usersidtagstagstopanswers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: id
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: path
        name: tags
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Tags
      - Answers
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---