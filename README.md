# SNCosmo Enhancement Proposals
 
EPs are documents to address non-trivial enhancements that require discussion and thought 
beyond a single Pull Request. This is intended to mirror the long-standing Python Enhancement 
Proposal process and Astropy's Proposals for Enhancement, but generally not quite as
formally as those much larger projects. Normally a proposal goes through various phases of 
consideration. Discussion is expected to take place using existing mechanisms (github, mailing 
list, etc), and eventually a decision is made regarding whether the proposal should be accepted, 
rejected, or tabled for further discussion later.

## Accepted EPs

| # |     Title                          | Date        | DOI   |
|---|:-----------------------------------|-------------|-------|
| 1 | [`Title`](url)                     | 2020-FEB-XX |[EP 1 DOI]()|
 
## Proposing a new EPs
 
New EPs should be created using the `sep-template.md` file in this repository. Fork the repository, 
copy `sep_template.md` to `EPs/sep_<some_working_name>.md` and issue a Pull Request with that file 
once you've written it up. Little explanation is required in the PR itself given that the document 
has all the content - usually it's easiest to just paste in the abstract. The EP number will be 
assigned once it is accepted.
 
Note that there is not much point to making proposals unless someone or some group has signed up to 
implement it if the EP is accepted (typically this would involve the author or authors of the EP). 
Just issuing an EP in order to spur others to do work is not generally going to be received well. 
Generally, an implementation is expected before an EP can be considered fully accepted. For proposals 
that require extensive work that few are willing to perform without some assurance it will be accepted, 
provisional acceptance is an option. For serious consideration it is usually good to show that detailed 
technical aspects have been played with in real code rather (even if it isn't a complete implementation).
 
 
## Finalizing EPs
 
The final decision on accepting, rejecting, or tabling an EPs lies with [Kyle Barbary](https://github.com/kbarbary). 
Once the community discussion on the EP has wound down, Kyle makes the
final decision on acceptance, rejection, or defering action. One of the community members should then:
 
1. Fill in the "Decision rationale" section of the EP with a description of why
   the EP was accepted, rejected or tabled, including a summary of the community's
   discussion as relevant.
2. Update the "date-last-revised" to the day of merging and "status" to
   "Accepted", "Rejected", or "Tabled".
3. If necessary, rename the EP file to be ``EP##.md``, where ## is the next
   free number on the list of EPs.
3. Leave a brief comment in the PR indicating the result.
3. Merge the PR with the above changes.
3. If the EP was accepted then continue with the remaining steps, otherwise stop now.
3. Upload the EP to Zenodo to give it a DOI.  Go to https://zenodo.org/deposit/new, upload
   the `.md` file, and set the fields to the following:
   
  | Zenodo field                  | Set to |
  | ------------------------------| -------|
  | Communities                   | The SNCosmo Project |
  | Upload type                   | Publication |
  | Publication type              | Technical note |
  | Publication Date              | The date-last-revised of the EP (which should be the same as the accepted date for new EPs) |
  | Title                         | SNCosmo Enhancement Proposals <number>: <title> (EP <number>) |
  | Authors                       | The EP authors (directly from the EP text, but with ORCIDs if possible) |
  | Description                   | The EP abstract (copy/paste the rendered HTML from GitHub) |
  | License                       | CC-Attribution (default) |
  | Related/alternate identifiers | Github link to the EP file *at the specific merge commit* as "is supplemented by this upload". If this is a revised version, this should be the URL of the commit where the EP was revised. |

8. Get the source for the DOI badge from the newly-created Zenodo record page by
   clicking on the DOI badge on the right side of the page and copying the
   markdown source.
9. On GitHub (or locally) edit ``README.md`` and add an entry for the new EP to the
   "Accepted EPs" table.  Use the DOI link from the previous step. Add
   corresponding Markdown link refs for both the DOI link and the new EP. Preview
   the update and test the links to make sure they are all correct. Then commit
   directly to master (or PR if you prefer).
10. Send an email to the [SNcosmo mailing list](mailto:sncosmo@googlegroups.com)
   announcing the acceptance In general this should just point to the accepted
   EP rather than providing additional decision rationale.
 
 
## Updating EPs
 
In the cases where an updated EP requires updating (e.g. references to a  new EP that 
supercedes it, clarifying information that emerges after the EP is accepted, etc.), changes 
can be made directly via PR, but the "date-last-revised" should be updated in the EP. Additionally, 
the Zenodo entry will need to be updated with a new version of the EP (*not* a completely 
new Zenodo entry), by using the "New version" button and then filling out the forms as described above.
 
 
This procedure was adapted from the [Astropy Proposals for Enhancement](https://github.com/astropy/astropy-APEs)
process.
