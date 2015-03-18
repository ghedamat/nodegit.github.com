---
layout: default
menu_item: api
title: Diff
description: Version 0.3.0
menu_item: api
return_to:
  "API Documentation Index": /api/
sections:
  "indexToWorkdir": "#indexToWorkdir"
  "treeToIndex": "#treeToIndex"
  "treeToTree": "#treeToTree"
  "treeToWorkdir": "#treeToWorkdir"
  "treeToWorkdirWithIndex": "#treeToWorkdirWithIndex"
  "#findSimilar": "#findSimilar"
  "#getDelta": "#getDelta"
  "#getPerfdata": "#getPerfdata"
  "#numDeltas": "#numDeltas"
  "#patches": "#patches"
  "DELTA": "#DELTA"
  "FIND": "#FIND"
  "FLAG": "#FLAG"
  "FORMAT": "#FORMAT"
  "FORMAT_EMAIL_FLAGS": "#FORMAT_EMAIL_FLAGS"
  "LINE": "#LINE"
  "OPTION": "#OPTION"
  "STATS_FORMAT": "#STATS_FORMAT"
---

## <a name="indexToWorkdir"></a><span>Diff.</span>indexToWorkdir <span class="tags"><span class="async">Async</span></span>

```js
Diff.indexToWorkdir(repo, index, opts).then(function(diff) {
  // Use diff
});
```

| Parameters | Type |   |
| --- | --- | --- |
| repo | [Repository](/api/repository/) | The repository. |
| index | [Index](/api/index/) | The index to diff from; repo index used if NULL. |
| opts | [DiffOptions](/api/diff_options/) | Structure with options to influence diff or NULL for defaults. |

| Returns |  |
| --- | --- |
| [Diff](/api/diff/) |  |

## <a name="treeToIndex"></a><span>Diff.</span>treeToIndex <span class="tags"><span class="async">Async</span></span>

```js
Diff.treeToIndex(repo, old_tree, index, opts).then(function(diff) {
  // Use diff
});
```

| Parameters | Type |   |
| --- | --- | --- |
| repo | [Repository](/api/repository/) | The repository containing the tree and index. |
| old_tree | [Tree](/api/tree/) | A git_tree object to diff from, or NULL for empty tree. |
| index | [Index](/api/index/) | The index to diff with; repo index used if NULL. |
| opts | [DiffOptions](/api/diff_options/) | Structure with options to influence diff or NULL for defaults. |

| Returns |  |
| --- | --- |
| [Diff](/api/diff/) |  |

## <a name="treeToTree"></a><span>Diff.</span>treeToTree <span class="tags"><span class="async">Async</span></span>

```js
Diff.treeToTree(repo, old_tree, new_tree, opts).then(function(diff) {
  // Use diff
});
```

| Parameters | Type |   |
| --- | --- | --- |
| repo | [Repository](/api/repository/) | The repository containing the trees. |
| old_tree | [Tree](/api/tree/) | A git_tree object to diff from, or NULL for empty tree. |
| new_tree | [Tree](/api/tree/) | A git_tree object to diff to, or NULL for empty tree. |
| opts | [DiffOptions](/api/diff_options/) | Structure with options to influence diff or NULL for defaults. |

| Returns |  |
| --- | --- |
| [Diff](/api/diff/) |  |

## <a name="treeToWorkdir"></a><span>Diff.</span>treeToWorkdir <span class="tags"><span class="async">Async</span></span>

```js
Diff.treeToWorkdir(repo, old_tree, opts).then(function(diff) {
  // Use diff
});
```

| Parameters | Type |   |
| --- | --- | --- |
| repo | [Repository](/api/repository/) | The repository containing the tree. |
| old_tree | [Tree](/api/tree/) | A git_tree object to diff from, or NULL for empty tree. |
| opts | [DiffOptions](/api/diff_options/) | Structure with options to influence diff or NULL for defaults. |

| Returns |  |
| --- | --- |
| [Diff](/api/diff/) |  |

## <a name="treeToWorkdirWithIndex"></a><span>Diff.</span>treeToWorkdirWithIndex <span class="tags"><span class="async">Async</span></span>

```js
Diff.treeToWorkdirWithIndex(repo, old_tree, opts).then(function(diff) {
  // Use diff
});
```

| Parameters | Type |   |
| --- | --- | --- |
| repo | [Repository](/api/repository/) | The repository containing the tree. |
| old_tree | [Tree](/api/tree/) | A git_tree object to diff from, or NULL for empty tree. |
| opts | [DiffOptions](/api/diff_options/) | Structure with options to influence diff or NULL for defaults. |

| Returns |  |
| --- | --- |
| [Diff](/api/diff/) |  |

## <a name="findSimilar"></a><span>Diff#</span>findSimilar <span class="tags"><span class="async">Async</span></span>

```js
diff.findSimilar(options).then(function(result) {
  // Use result
});
```

| Parameters | Type |
| --- | --- | --- |
| options | [DiffFindOptions](/api/diff_find_options/) | Control how detection should be run, NULL for defaults |

| Returns |  |
| --- | --- |
| Number |  0 on success, -1 on failure |

## <a name="getDelta"></a><span>Diff#</span>getDelta <span class="tags"><span class="sync">Sync</span></span>

```js
var diffDelta = diff.getDelta(idx);
```

| Parameters | Type |
| --- | --- | --- |
| idx | Number | Index into diff list |

| Returns |  |
| --- | --- |
| [DiffDelta](/api/diff_delta/) |  |

## <a name="getPerfdata"></a><span>Diff#</span>getPerfdata <span class="tags"><span class="async">Async</span></span>

```js
diff.getPerfdata().then(function(diffPerfdata) {
  // Use diffPerfdata
});
```

| Returns |  |
| --- | --- |
| [DiffPerfdata](/api/diff_perfdata/) | Structure to be filled with diff performance data |

## <a name="numDeltas"></a><span>Diff#</span>numDeltas <span class="tags"><span class="sync">Sync</span></span>

```js
var result = diff.numDeltas();
```

| Returns |  |
| --- | --- |
| Number |  Count of number of deltas in the list |

## <a name="patches"></a><span>Diff#</span>patches <span class="tags"><span class="sync">Sync</span></span>

```js
var convenientPatch = diff.patches();
```

Retrieve patches in this difflist


| Returns |  |
| --- | --- |
| [ConvenientPatch](/api/convenient_patch/) | an array of ConvenientPatches |

## <a name="DELTA"></a><span>Diff.</span>DELTA <span class="tags"><span class="enum">ENUM</span></span>

| Flag | Value |
| --- | --- | --- |
| <span>Diff.DELTA.</span>UNMODIFIED | 0 |
| <span>Diff.DELTA.</span>ADDED | 1 |
| <span>Diff.DELTA.</span>DELETED | 2 |
| <span>Diff.DELTA.</span>MODIFIED | 3 |
| <span>Diff.DELTA.</span>RENAMED | 4 |
| <span>Diff.DELTA.</span>COPIED | 5 |
| <span>Diff.DELTA.</span>IGNORED | 6 |
| <span>Diff.DELTA.</span>UNTRACKED | 7 |
| <span>Diff.DELTA.</span>TYPECHANGE | 8 |
| <span>Diff.DELTA.</span>UNREADABLE | 9 |

## <a name="FIND"></a><span>Diff.</span>FIND <span class="tags"><span class="enum">ENUM</span></span>

| Flag | Value |
| --- | --- | --- |
| <span>Diff.FIND.</span>BY_CONFIG | 0 |
| <span>Diff.FIND.</span>RENAMES | 1 |
| <span>Diff.FIND.</span>RENAMES_FROM_REWRITES | 2 |
| <span>Diff.FIND.</span>COPIES | 4 |
| <span>Diff.FIND.</span>COPIES_FROM_UNMODIFIED | 8 |
| <span>Diff.FIND.</span>REWRITES | 16 |
| <span>Diff.FIND.</span>BREAK_REWRITES | 32 |
| <span>Diff.FIND.</span>AND_BREAK_REWRITES | 48 |
| <span>Diff.FIND.</span>FOR_UNTRACKED | 64 |
| <span>Diff.FIND.</span>ALL | 255 |
| <span>Diff.FIND.</span>IGNORE_LEADING_WHITESPACE | 0 |
| <span>Diff.FIND.</span>IGNORE_WHITESPACE | 4096 |
| <span>Diff.FIND.</span>DONT_IGNORE_WHITESPACE | 8192 |
| <span>Diff.FIND.</span>EXACT_MATCH_ONLY | 16384 |
| <span>Diff.FIND.</span>BREAK_REWRITES_FOR_RENAMES_ONLY | 32768 |
| <span>Diff.FIND.</span>REMOVE_UNMODIFIED | 65536 |

## <a name="FLAG"></a><span>Diff.</span>FLAG <span class="tags"><span class="enum">ENUM</span></span>

| Flag | Value |
| --- | --- | --- |
| <span>Diff.FLAG.</span>BINARY | 1 |
| <span>Diff.FLAG.</span>NOT_BINARY | 2 |
| <span>Diff.FLAG.</span>VALID_ID | 4 |

## <a name="FORMAT"></a><span>Diff.</span>FORMAT <span class="tags"><span class="enum">ENUM</span></span>

| Flag | Value |
| --- | --- | --- |
| <span>Diff.FORMAT.</span>PATCH | 1 |
| <span>Diff.FORMAT.</span>PATCH_HEADER | 2 |
| <span>Diff.FORMAT.</span>RAW | 3 |
| <span>Diff.FORMAT.</span>NAME_ONLY | 4 |
| <span>Diff.FORMAT.</span>NAME_STATUS | 5 |

## <a name="FORMAT_EMAIL_FLAGS"></a><span>Diff.</span>FORMAT_EMAIL_FLAGS <span class="tags"><span class="enum">ENUM</span></span>

| Flag | Value |
| --- | --- | --- |
| <span>Diff.FORMAT_EMAIL_FLAGS.</span>FORMAT_EMAIL_NONE | 0 |
| <span>Diff.FORMAT_EMAIL_FLAGS.</span>FORMAT_EMAIL_EXCLUDE_SUBJECT_PATCH_MARKER | 1 |

## <a name="LINE"></a><span>Diff.</span>LINE <span class="tags"><span class="enum">ENUM</span></span>

| Flag | Value |
| --- | --- | --- |
| <span>Diff.LINE.</span>CONTEXT | 32 |
| <span>Diff.LINE.</span>ADDITION | 43 |
| <span>Diff.LINE.</span>DELETION | 45 |
| <span>Diff.LINE.</span>CONTEXT_EOFNL | 61 |
| <span>Diff.LINE.</span>ADD_EOFNL | 62 |
| <span>Diff.LINE.</span>DEL_EOFNL | 60 |
| <span>Diff.LINE.</span>FILE_HDR | 70 |
| <span>Diff.LINE.</span>HUNK_HDR | 72 |
| <span>Diff.LINE.</span>BINARY | 66 |

## <a name="OPTION"></a><span>Diff.</span>OPTION <span class="tags"><span class="enum">ENUM</span></span>

| Flag | Value |
| --- | --- | --- |
| <span>Diff.OPTION.</span>NORMAL | 0 |
| <span>Diff.OPTION.</span>REVERSE | 1 |
| <span>Diff.OPTION.</span>INCLUDE_IGNORED | 2 |
| <span>Diff.OPTION.</span>RECURSE_IGNORED_DIRS | 4 |
| <span>Diff.OPTION.</span>INCLUDE_UNTRACKED | 8 |
| <span>Diff.OPTION.</span>RECURSE_UNTRACKED_DIRS | 16 |
| <span>Diff.OPTION.</span>INCLUDE_UNMODIFIED | 32 |
| <span>Diff.OPTION.</span>INCLUDE_TYPECHANGE | 64 |
| <span>Diff.OPTION.</span>INCLUDE_TYPECHANGE_TREES | 128 |
| <span>Diff.OPTION.</span>IGNORE_FILEMODE | 256 |
| <span>Diff.OPTION.</span>IGNORE_SUBMODULES | 512 |
| <span>Diff.OPTION.</span>IGNORE_CASE | 1024 |
| <span>Diff.OPTION.</span>DISABLE_PATHSPEC_MATCH | 4096 |
| <span>Diff.OPTION.</span>SKIP_BINARY_CHECK | 8192 |
| <span>Diff.OPTION.</span>ENABLE_FAST_UNTRACKED_DIRS | 16384 |
| <span>Diff.OPTION.</span>UPDATE_INDEX | 32768 |
| <span>Diff.OPTION.</span>INCLUDE_UNREADABLE | 65536 |
| <span>Diff.OPTION.</span>INCLUDE_UNREADABLE_AS_UNTRACKED | 131072 |
| <span>Diff.OPTION.</span>FORCE_TEXT | 1048576 |
| <span>Diff.OPTION.</span>FORCE_BINARY | 2097152 |
| <span>Diff.OPTION.</span>IGNORE_WHITESPACE | 4194304 |
| <span>Diff.OPTION.</span>IGNORE_WHITESPACE_CHANGE | 8388608 |
| <span>Diff.OPTION.</span>IGNORE_WHITESPACE_EOL | 16777216 |
| <span>Diff.OPTION.</span>SHOW_UNTRACKED_CONTENT | 33554432 |
| <span>Diff.OPTION.</span>SHOW_UNMODIFIED | 67108864 |
| <span>Diff.OPTION.</span>PATIENCE | 268435456 |
| <span>Diff.OPTION.</span>MINIMAL | 536870912 |
| <span>Diff.OPTION.</span>SHOW_BINARY | 1073741824 |

## <a name="STATS_FORMAT"></a><span>Diff.</span>STATS_FORMAT <span class="tags"><span class="enum">ENUM</span></span>

| Flag | Value |
| --- | --- | --- |
| <span>Diff.STATS_FORMAT.</span>STATS_NONE | 0 |
| <span>Diff.STATS_FORMAT.</span>STATS_FULL | 1 |
| <span>Diff.STATS_FORMAT.</span>STATS_SHORT | 2 |
| <span>Diff.STATS_FORMAT.</span>STATS_NUMBER | 4 |
| <span>Diff.STATS_FORMAT.</span>STATS_INCLUDE_SUMMARY | 8 |
