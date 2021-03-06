# Commands : Patches: How to use JavaScript to patch your documents?

**Patch** command is used to perform partial document updates without having to load, modify, and save a full document. This is usually useful for updating denormalized data in entities.

## Syntax

{CODE patch_1@ClientApi\Commands\Patches\Javascript.cs /}

**Parameters**

{CODE scriptedpatchrequest@Common.cs /}

## Methods, objects and variables

Before we will move to the examples, let's look at the methods, objects, and variables available:

| ------ |:------:| ------ |
| `__document_id` | variable | Id for current document |
| `this` | object | Current document (with metadata) |
| `LoadDocument(key)` | method | Allows document loading, increases maximum number of allowed steps in script. See `Raven/AdditionalStepsForScriptBasedOnDocumentSize` [here](../../../server/configuration/configuration-options#javascript-parser). |
| `PutDocument(key, data, metadata)` | method | Allows document putting, returns generated key |
| `IncreaseNumberOfAllowedStepsBy(number)` | method | Will increase the maximum allowed number of steps in script by given value. Only available if `Raven/AllowScriptsToAdjustNumberOfSteps` is set to `true`. |
| `_` | object | [Lo-Dash](https://lodash.com/) |
| `trim()` | string.prototype | trims the string e.g. `this.FirstName.trim()` |
| `indexOf(...)` | Array.prototype | wrapper for [_.indexOf](https://lodash.com/docs#indexOf) |
| `filter(...)` | Array.prototype | wrapper for [_.filter](https://lodash.com/docs#filter) |
| `Map(...)` | Array.prototype | wrapper for [_.map](https://lodash.com/docs#map) |
| `Where(...)` | Array.prototype | wrapper for [_.filter](https://lodash.com/docs#filter) |
| `RemoveWhere(...)` | Array.prototype | wrapper for [_.remove](https://lodash.com/docs#remove) returning Array for easier chaining |
| `Remove(...)` | Array.prototype | wrapper for [_.pull](https://lodash.com/docs#pull) returning Array for easier chaining |

## Custom functions

Beside built-in functions, custom ones can be introduced. Please visit [this](../../../studio/overview/settings/custom-functions) page if you want to know how to add custom functions.

## Example I

{CODE patch_2@ClientApi\Commands\Patches\Javascript.cs /}

## Example II

{CODE patch_3@ClientApi\Commands\Patches\Javascript.cs /}

## Example III

{CODE patch_4@ClientApi\Commands\Patches\Javascript.cs /}

## Example IV

{CODE patch_5@ClientApi\Commands\Patches\Javascript.cs /}

## Example V

{CODE patch_6@ClientApi\Commands\Patches\Javascript.cs /}

## Example VI

{CODE patch_7@ClientApi\Commands\Patches\Javascript.cs /}

## Example VII

{CODE patch_8@ClientApi\Commands\Patches\Javascript.cs /}

## Example VIII

{CODE patch_9@ClientApi\Commands\Patches\Javascript.cs /}

## Example IX

{CODE patch_1_0@ClientApi\Commands\Patches\Javascript.cs /}

## Example X

{CODE patch_1_1@ClientApi\Commands\Patches\Javascript.cs /}

## Example XI

{CODE patch_1_2@ClientApi\Commands\Patches\Javascript.cs /}

## Related articles

- [How to work with **patch requests**?](../../../client-api/commands/patches/how-to-work-with-patch-requests) 
- [Studio : How to add **custom functions**?](../../../studio/overview/settings/custom-functions)
