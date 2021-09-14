# How we set salaries

Salaries are an integral part of the Employee Value Proposition. The ultimate goal in setting a salary is to seek alignment between employer and employee such that we don't need to have conversations about salary. If an employee feels underpaid, that's a problem. If they feel overpaid, that's also a problem. Efficient salary programs are fair and transparent. This is what we aspire to at Bench.

[Read the blog post about how and why we created this system](https://medium.com/lifeatbench/we-built-a-tool-to-help-us-foster-growth-in-our-engineers-45879e4a9892)

## Market Value and Competency

At Bench, there are two key components of salary: market value and competency. **Market value** is a driven by the demand that exists for the skills that you have. **Competency** is the level of competency that you have within to the role that you've been hired to fill.

### How we determine market value

The first step in determining market value is clearly defining the roles in your organization. At Bench we chose to use numbered levels for our engineers—we go from Engineer 1 to Engineer 5. For each level, we defined a very clear set of competencies (see [Competencies by Role](https://docs.google.com/spreadsheets/d/1rV2q8TJaY8gHhuAhXaHBLJdld3XLdJG-UbL706SkCAY/edit#gid=221997572)).

Once our roles were clearly defined, we compared them to the two salary databases that we purchase on an annual basis (Radford and HR Tech). Salary databases collect data from thousands of companies each year. For each job title, they provide the median and mean salaries at the 50th, 75th, and 90th percentile. The basic idea is that you find matches in their database for the roles in your organization, and then use their data to set a competitive salary midpoint—in our case, at the 75th percentile.

Salary databases are useful tools for creating a competitive salary program, but they need to be taken with a grain of salt. Job titles are non-standard, and often company-size-dependent. For example, a CTO at a 5-person startup is a very different job from a CTO with a 1000-person engineering team. We've learned that it's rare to find a perfect match with a job title in the database, so the trick is to find those that are closest, and then use a combination of other sources (job postings, exit interviews, and gut instinct) to set the salary midpoint.

Once we've chosen the salary midpoint for a role, creating salary bands is trivial. At Bench, a salary band is from 0.8 to 1.2 of the salary midpoint. For example, if a midpoint is $100,000, the band is $80,000 - $120,000.

### How we determine competency

Salary bands set the market context for a role, and competency determines an employee's location within the band. We use the competencies that we defined for each role to determine an employee's competency on an annual basis. Here's how it works: 

- Team member does a self-assessment, rating themselves between 1-5 for each competency in their role
- Their manager does the same assessment
- They meet to talk about each competency, and negotiate the score for that competency
- We use their average score to calculate their position in the band (0.8-1.2) using a [default open formula](https://docs.google.com/spreadsheets/d/1hqgSXq_WTfHes5P3Ep_4kC6m-UUIjwM4A-xyoWUfbiI/edit#gid=658533355&range=A1). We call this number the _compa-ratio_
- We then multiply the salary midpoint by their compa-ratio to determine salary

This bullet list looks quite simple, but in reality these sessions are full of deeply honest conversations about growth. They help us create growth goals, they specify areas of focus, and they ensure that every salary decision that we make is backed by a transparent, documented, and repeatable process.

[See our Competency Assessment template](https://docs.google.com/spreadsheets/d/1hqgSXq_WTfHes5P3Ep_4kC6m-UUIjwM4A-xyoWUfbiI/edit#gid=0)

### How do we handle changes in market value?

If the market changes and salary midpoints are higher, we can simply multiply these midpoints by the compa-ratio to determine updated salaries. This is significantly more efficient than re-reviewing every person every time the market changes. It's also worth noting that we never decrease salaries when the market goes down.

We review market data and updating salary bands at least once per year.

## Promotions

Salary bands can be large, and this is on purpose. They are designed to overlap each other. Here’s a visualization with dummy data:

![Image of salary Bands](images/bands.png)

This is useful for a number of reasons:

- It gives us flexibility to promote early to encourage growth
- In situations where positions are potentially limited, like Engineering Managers, it allows us to continue to give salary increases while we seek out a promotion opportunity.
- A “downside” of overlapping bands is that promotions don’t come with massive salary increases. This is actually an upside, because it allows us to steadily hand more and more responsibility to a team member as they approach the promotion threshold, such that when we do finally make the leap, the transition is much smoother for all parties.
- There isn’t a hard compa-ratio cutoff for promotion. Each case will be evaluated individually based on the current available positions, the needs of the team, and the interest of the individual. When the promotion occurs, the team member will go through the competency assessment process for their new role to determine compensation.
