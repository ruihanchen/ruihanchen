# Hello! <img src="https://github.com/ruihanchen/ruihanchen/blob/main/wave.gif" width=50> I'm Ruihan Chen.
[![Linkedin](https://img.shields.io/badge/-ruihanchen-blue?style=flat&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/ruihanchen/)
[![Gmail](https://img.shields.io/badge/-ruihanchen@berkeley.edu-c14438?style=flat&logo=Gmail&logoColor=white)](mailto:ruihanchen@berkeley.edu)
[![Blog](https://img.shields.io/badge/-https://github.com/ruihanchen-black?style=flat&labelColor=black&logo=github&logoColor=white)](https://github.com/ruihanchen)

## <img src = "https://user-images.githubusercontent.com/63050133/156777293-72a6e681-2582-4a9d-ad92-09d1181d47c7.gif" width = 50>  About me
 
UC Berkeley, Data Science B.A. · Backend systems
 
Everything here started as a question I couldn't answer by reading about it.
How does git actually store a commit? When does thread-per-request beat an
event loop? Why did Ticketmaster fall over? I rebuild the thing to find out,
then measure whether I was right.
 
Java · Spring Boot · Python · PostgreSQL · Redis · React · TypeScript · Docker
 
---

**[QueryPilot](https://github.com/ruihanchen/QueryPilot)** — Text-to-SQL over
Postgres that turned into a project about the dependency instead. Skipped
self-consistency after measuring what it would catch: at temperature 0 the SQL
comes back identical, and the failure that actually bites was in all three
samples. Sampling can't catch a mistake every sample shares. The model wrote
`DELETE FROM restaurants` early on; a foreign key was the only reason the data
survived.
 
**[TicketFlow](https://github.com/ruihanchen/TicketFlow)** — Flash-sale
backend, started after the 2022 Ticketmaster meltdown. Rewrote the inventory
path three times. Shipped a Redis dual-write at 2.4x throughput, then tore it
out when I realized the crash mode had no recovery path. CDC via Debezium
instead. Killed the JVM mid-run to check whether Redis actually converges
back to Postgres. It does.
 
**[NioStore](https://github.com/ruihanchen/niostore)** — Redis-compatible KV
server, no production dependencies. Started on Java 17 to understand how one
thread serves many connections; when Java 21 shipped virtual threads I added
a second implementation to settle an argument I kept seeing but never
measured. Under a 10ms downstream call: 35,461 req/s vs 95. Remove the call
and the event loop wins. Three ADRs, one devlog with the wrong turns left in.
 
**[NearBite](https://github.com/ruihanchen/NearBite)** — Full-stack delivery
app built around Berkeley restaurants I actually go to. V1 in 2022; came back
after two years of code reviews at work and rewrote it. The Redis cart here is
deliberately *not* the TicketFlow approach — same consistency problem,
different answer, and the README says why.
 
**[pit](https://github.com/ruihanchen/pit)** — Git-compatible VCS in Python,
written after chapter 10 of Pro Git to see how far I could get. Binary v2
index, Myers O(ND) diff, three-way merge with LCA. `git log` works on a pit
repo. Revisited in 2023: adding type annotations surfaced a merge bug that
`dict[str, Any]` had been hiding.
 
**[GitPulse](https://github.com/ruihanchen/gitpulse)** — GitHub org analytics.
Bus factor, PR turnaround percentiles, async ingestion.
 
---
 
Every README has a "What's Still Missing" section. I find those more
interesting than the parts that work.

<br> 

---

<p align = "center">
	<a href="https://github.com/piyushsuthar/github-readme-quotes"> <img alt = "Quote" src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight&animation=grow_out_in&quoteCategory=programming">
</p>

</details>

</br></br>
	
