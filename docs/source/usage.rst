Usage
=====

.. _api-secret:

Obtain a secret
------------

To make a request to this API you must first obtain a secret. Within every request you make
you will pass this secret as an paramater insuring your status!

Traditional Auth will be implemented as this project develops.

To request a secret please email ``matthew@suade.tech`` and follow the instructions that follow.


Making a request
----------------

To make a request to our api you'll use a ``GET`` request to the url ``https://suade-tech.herokuapp.com/ask``.
There are two required parameters will be ``secret``, and ``prompt``. enter in your secret within the ``secret`` 
paramter and any request you'd like to ask our generative ai within the ``prompt`` paramater.

For example:

>>> import requests
>>> url = 'https://suade-tech.herokuapp.com/ask'
>>> params = {
            'prompt': 'How can I become a better sales person?',
            'secret': 'SECRET'
         }
>>> response = requests.get(url, params=params)
>>> if response.status_code == 200:
>>>    print(response.content)
>>> else:
>>>    print(f'Request failed with status code {response.status_code}.')
[- Know your product or service in depth: Learn all about the features, benefits and unique selling points of what you're
selling. This will boost your credibility and make it easier to answer any questions from potential customers.

- Listen actively: Pay close attention to what your customers are saying, and try to understand their needs and
expectations. This will help you tailor your approach and make them feel valued.

- Build relationships: Foster good relationships with your customers by cultivating trust, establishing genuine
connections and creating positive experiences.

- Focus on solving problems: Instead of making a hard sell, concentrate on how your product or service can solve
problems for your customers. This will make them more likely to invest in your offerings.

- Stay up-to-date with industry trends: Keep an eye on emerging trends, technology, and customer needs and adapt
accordingly, so you can stay ahead of the curve and provide better service.

- Invest in yourself: Continuously improve and develop your skills with training courses, reading literature, and going
to seminars aimed at improving your sales skills.]

In the example above you would replace ``SECRET`` with your secret UUID

or for a curl request:
>>> curl --location 'https://suade-tech.herokuapp.com/ask?prompt=how%20can%20I%20become%20a%20beter%20sales%20person%3F&secret=SECRET'

In the example above you would replace ``SECRET`` with your secret UUID
