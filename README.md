# Awesome Logseq DB 🚀

A curated list of awesome plugins, themes, resources, and SQLite tools specifically verified for the Logseq 2.0 Database architecture.

## 🔌 Database-Ready Plugins
* [Plugin Name](link) - One sentence description highlighting 2.0 DB compatibility.
* https://github.com/kerim/logseq-db-sidekick

## 🎨 Layout-Verified Themes
* [Theme Name](link) - Clean themes that support the new multi-pane DB layout without visual bugs.

## 📊 SQLite & Datalog Queries
### 📅 Active Task Dashboard
Copy and paste this advanced query block into any Logseq 2.0 page to display a clean dashboard of your ongoing tasks sorted by priority.

```clojure
#+BEGIN_QUERY
{:title [:h3 "📥 Active Database Tasks"]
 :query [:find (pull ?b [*])
         :where
         [?b :block/marker ?marker]
         [(contains? #{"NOW" "LATER" "TODO" "DOING"} ?marker)]]
 :result-transform (fn [res]
                     (sort-by (fn [b] (get b :block/priority "Z")) res))
 :collapsed? false}
#+END_QUERY
```


## 🐳 Self-Hosting & Docker
* [Tool Name](link) - Infrastructure scripts for hosting your own graph sync servers.
