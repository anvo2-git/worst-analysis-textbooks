# Reflection Questions

## 1. What files make up your site and what does each one do?

The root of the site has an `index.html` and `style.css` that serve as the gallery page. It organises all 26 landing page versions into three phases (Go Wide, Combine, Polish) and links to each one. There's also a `CLAUDE.md` that contains project instructions and design constraints I gave Claude Code, and a `review-content.md` file that acts as a content bank of adapted Reddit-style fake reviews used across versions. Then there are 26 folders (`v1/` through `v26/`), each containing its own `index.html` and `style.css`. One self-contained landing page per folder. Every page is pure HTML and CSS with no external dependencies, no JavaScript, and no CDNs.

## 2. Describe the pipeline: what happens from git push to your site updating on Vercel?

When I run `git push`, my local commits get sent to the GitHub repository. Vercel is connected to that repo via a webhook, so it automatically detects the new push. Since this is a static site with no build step or framework, Vercel just takes the files as-is and deploys them to its CDN. Within about 30 to 60 seconds the new version is live at my Vercel URL. Every push creates a new deployment, and Vercel keeps previous deployments around so you could roll back if needed.

## 3. Justify your final version. After your entire exploration, why did you land on this version?

In Phase 1, I told Claude to go wild, so it went with a standard but diverse catalogue. Brutalist neon, retro Y2K, government safety notices, horror movie posters, a conspiracy corkboard, a Yahoo 360 blog. Most of the flamboyant ones felt like too much for a site on sarcastic maths content. I gravitated towards simpler, cleaner designs. My favourites ended up being v6 (dark luxury editorial), v9 (MathAdvisor/Yelp parody), v10 (Yahoo 360 blog), and v19 (light academic blog). I also had Claude do some research on popular meme Reddit posts to paraphrase into book reviews, which gave the content a recognisable, internet-native voice.

In Phase 2, I combined elements from those favourites into 7 hybrids. v19, a warm, Substack-style academic blog called "The Epsilon Errata," won out because the format let the writing carry the page. The humour and personality came through the content, not flashy design tricks. A single-column serif blog with cream backgrounds and burgundy accents was the right container for sarcastic textbook reviews.

Phase 3 refined v19 across six iterations: typography, curated content from the review bank, visual polish (paper texture, star ratings, pull quotes), layout enhancements (drop caps, post numbers), and responsive design with micro-interactions. The final version (v26) added the content touches that brought it together: reviews posted on holidays like Christmas and Valentine's Day, Reddit-style edits, reader comments, emojis used sparingly, one genuinely profane review, and an About the Author section revealing the blogger now raises cattle in Montana. It ends with "Today You, Tomorrow Me," a sincere, emotional review that lands because everything before it is funny. That contrast is the whole point of the site.
