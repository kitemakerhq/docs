# Kitemaker GraphQL API

This API is currently in private alpha and subject to change

<details>
  <summary><strong>Table of Contents</strong></summary>

  * [Query](#query)
  * [Mutation](#mutation)
  * [Objects](#objects)
    * [AddLabelsToWorkItemResult](#addlabelstoworkitemresult)
    * [AddMembersToWorkItemResult](#addmemberstoworkitemresult)
    * [AddWatchersToThemeResult](#addwatcherstothemeresult)
    * [AddWatchersToWorkItemResult](#addwatcherstoworkitemresult)
    * [AddWorkItemsToThemeResult](#addworkitemstothemeresult)
    * [Application](#application)
    * [Comment](#comment)
    * [CreateCommentOnThemeResult](#createcommentonthemeresult)
    * [CreateCommentOnWorkItemResult](#createcommentonworkitemresult)
    * [CreateThemeResult](#createthemeresult)
    * [CreateWorkItemResult](#createworkitemresult)
    * [EditCommentResult](#editcommentresult)
    * [EditThemeResult](#editthemeresult)
    * [EditWorkItemResult](#editworkitemresult)
    * [Integration](#integration)
    * [IntegrationUser](#integrationuser)
    * [Label](#label)
    * [Organization](#organization)
    * [RemoveLabelsFromWorkItemResult](#removelabelsfromworkitemresult)
    * [RemoveMembersFromWorkItemResult](#removemembersfromworkitemresult)
    * [RemoveWatchersFromThemeResult](#removewatchersfromthemeresult)
    * [RemoveWatchersFromWorkItemResult](#removewatchersfromworkitemresult)
    * [RemoveWorkItemsFromThemeResult](#removeworkitemsfromthemeresult)
    * [Space](#space)
    * [Status](#status)
    * [Theme](#theme)
    * [ThemesQueryResult](#themesqueryresult)
    * [User](#user)
    * [WorkItem](#workitem)
    * [WorkItemsQueryResult](#workitemsqueryresult)
  * [Inputs](#inputs)
    * [AddLabelsToWorkItemInput](#addlabelstoworkiteminput)
    * [AddMembersToWorkItemInput](#addmemberstoworkiteminput)
    * [AddWatchersToThemeInput](#addwatcherstothemeinput)
    * [AddWatchersToWorkItemInput](#addwatcherstoworkiteminput)
    * [AddWorkItemsToThemeInput](#addworkitemstothemeinput)
    * [CreateCommentOnThemeInput](#createcommentonthemeinput)
    * [CreateCommentOnWorkItemInput](#createcommentonworkiteminput)
    * [CreateThemeInput](#createthemeinput)
    * [CreateWorkItemInput](#createworkiteminput)
    * [EditCommentInput](#editcommentinput)
    * [EditThemeInput](#editthemeinput)
    * [EditWorkItemInput](#editworkiteminput)
    * [RemoveLabelsFromWorkItemInput](#removelabelsfromworkiteminput)
    * [RemoveMembersFromWorkItemInput](#removemembersfromworkiteminput)
    * [RemoveWatchersFromThemeInput](#removewatchersfromthemeinput)
    * [RemoveWatchersFromWorkItemInput](#removewatchersfromworkiteminput)
    * [RemoveWorkItemsFromThemeInput](#removeworkitemsfromthemeinput)
  * [Enums](#enums)
    * [CacheControlScope](#cachecontrolscope)
    * [EffortSize](#effortsize)
    * [ImpactSize](#impactsize)
    * [IntegrationType](#integrationtype)
    * [StatusType](#statustype)
    * [ThemeHorizon](#themehorizon)
  * [Scalars](#scalars)
    * [Boolean](#boolean)
    * [Date](#date)
    * [ID](#id)
    * [Int](#int)
    * [String](#string)
    * [Upload](#upload)

</details>

## Query
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>organization</strong></td>
<td valign="top"><a href="#organization">Organization</a>!</td>
<td>

Fetch the main organization object. Useful for finding out which users, spaces, labels, statuses, etc. are available before fetching and manipulating work items and themes

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>workItems</strong></td>
<td valign="top"><a href="#workitemsqueryresult">WorkItemsQueryResult</a>!</td>
<td>

Fetch [WorkItem](#workitem) objects for a particular [Space](#space). This will return at most 50 work items at a time so use the paging facilities to fetch more results

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">spaceId</td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">cursor</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">count</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>workItem</strong></td>
<td valign="top"><a href="#workitem">WorkItem</a>!</td>
<td>

Fetch a single [WorkItem](#workitem) by ID

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>themes</strong></td>
<td valign="top"><a href="#themesqueryresult">ThemesQueryResult</a>!</td>
<td>

Fetch [Theme](#theme) objects for a particular [Space](#space). This will return at most 50 themes at a time so use the paging facilities to fetch more results

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">spaceId</td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">cursor</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">count</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>theme</strong></td>
<td valign="top"><a href="#theme">Theme</a>!</td>
<td>

Fetch a single [Theme](#theme) by ID

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Mutation
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createWorkItem</strong></td>
<td valign="top"><a href="#createworkitemresult">CreateWorkItemResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createworkiteminput">CreateWorkItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>editWorkItem</strong></td>
<td valign="top"><a href="#editworkitemresult">EditWorkItemResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#editworkiteminput">EditWorkItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>addMembersToWorkItem</strong></td>
<td valign="top"><a href="#addmemberstoworkitemresult">AddMembersToWorkItemResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#addmemberstoworkiteminput">AddMembersToWorkItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>removeMembersFromWorkItem</strong></td>
<td valign="top"><a href="#removemembersfromworkitemresult">RemoveMembersFromWorkItemResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#removemembersfromworkiteminput">RemoveMembersFromWorkItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>addWatchersToWorkItem</strong></td>
<td valign="top"><a href="#addwatcherstoworkitemresult">AddWatchersToWorkItemResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#addwatcherstoworkiteminput">AddWatchersToWorkItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>removeWatchersFromWorkItem</strong></td>
<td valign="top"><a href="#removewatchersfromworkitemresult">RemoveWatchersFromWorkItemResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#removewatchersfromworkiteminput">RemoveWatchersFromWorkItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>addLabelsToWorkItem</strong></td>
<td valign="top"><a href="#addmemberstoworkitemresult">AddMembersToWorkItemResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#addlabelstoworkiteminput">AddLabelsToWorkItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>removeLabelsFromWorkItem</strong></td>
<td valign="top"><a href="#removelabelsfromworkitemresult">RemoveLabelsFromWorkItemResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#removelabelsfromworkiteminput">RemoveLabelsFromWorkItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createCommentOnWorkItem</strong></td>
<td valign="top"><a href="#createcommentonworkitemresult">CreateCommentOnWorkItemResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createcommentonworkiteminput">CreateCommentOnWorkItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createTheme</strong></td>
<td valign="top"><a href="#createthemeresult">CreateThemeResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createthemeinput">CreateThemeInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>editTheme</strong></td>
<td valign="top"><a href="#editthemeresult">EditThemeResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#editthemeinput">EditThemeInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>addWatchersToTheme</strong></td>
<td valign="top"><a href="#addwatcherstothemeresult">AddWatchersToThemeResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#addwatcherstothemeinput">AddWatchersToThemeInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>removeWatchersFromTheme</strong></td>
<td valign="top"><a href="#removewatchersfromthemeresult">RemoveWatchersFromThemeResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#removewatchersfromthemeinput">RemoveWatchersFromThemeInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>addWorkItemsToTheme</strong></td>
<td valign="top"><a href="#addworkitemstothemeresult">AddWorkItemsToThemeResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#addworkitemstothemeinput">AddWorkItemsToThemeInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>removeWorkItemsFromTheme</strong></td>
<td valign="top"><a href="#removeworkitemsfromthemeresult">RemoveWorkItemsFromThemeResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#removeworkitemsfromthemeinput">RemoveWorkItemsFromThemeInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createCommentOnTheme</strong></td>
<td valign="top"><a href="#createcommentonthemeresult">CreateCommentOnThemeResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createcommentonthemeinput">CreateCommentOnThemeInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>editComment</strong></td>
<td valign="top"><a href="#editcommentresult">EditCommentResult</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#editcommentinput">EditCommentInput</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Objects

### AddLabelsToWorkItemResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>workItem</strong></td>
<td valign="top"><a href="#workitem">WorkItem</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AddMembersToWorkItemResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>workItem</strong></td>
<td valign="top"><a href="#workitem">WorkItem</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AddWatchersToThemeResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>theme</strong></td>
<td valign="top"><a href="#theme">Theme</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AddWatchersToWorkItemResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>workItem</strong></td>
<td valign="top"><a href="#workitem">WorkItem</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AddWorkItemsToThemeResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>theme</strong></td>
<td valign="top"><a href="#theme">Theme</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Application

Applications represent some service/code/etc that integrates with Kitemaker. You maybe even have one if you're reading these documents

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Comment

Comments can be made on either [WorkItem](#workitem) or [Theme](#theme) objects

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>actor</strong></td>
<td valign="top"><a href="#actor">Actor</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>body</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>threadId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Comments in Kitemaker are threaded and the threadId identifies a set of comments in a single thread

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateCommentOnThemeResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>comment</strong></td>
<td valign="top"><a href="#comment">Comment</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateCommentOnWorkItemResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>comment</strong></td>
<td valign="top"><a href="#comment">Comment</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateThemeResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>theme</strong></td>
<td valign="top"><a href="#theme">Theme</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateWorkItemResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>workItem</strong></td>
<td valign="top"><a href="#workitem">WorkItem</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### EditCommentResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>comment</strong></td>
<td valign="top"><a href="#comment">Comment</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### EditThemeResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>theme</strong></td>
<td valign="top"><a href="#theme">Theme</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### EditWorkItemResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>workItem</strong></td>
<td valign="top"><a href="#workitem">WorkItem</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Integration

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#integrationtype">IntegrationType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>domain</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### IntegrationUser

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#integrationtype">IntegrationType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>domain</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

The domain of a particular integration for systems like GitHub enterprise where each customer has a dedicated URL

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>externalId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

The ID of the user in the external system (such as Slack or GitHub)

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>externalName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

The name of the user in the external system (such as Slack or GitHub)

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Label

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>color</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Organization

The top level object describing the user or application's organization

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>spaces</strong></td>
<td valign="top">[<a href="#space">Space</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>users</strong></td>
<td valign="top">[<a href="#user">User</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>integrations</strong></td>
<td valign="top">[<a href="#integration">Integration</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>integrationUsers</strong></td>
<td valign="top">[<a href="#integrationuser">IntegrationUser</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RemoveLabelsFromWorkItemResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>workItem</strong></td>
<td valign="top"><a href="#workitem">WorkItem</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RemoveMembersFromWorkItemResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>workItem</strong></td>
<td valign="top"><a href="#workitem">WorkItem</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RemoveWatchersFromThemeResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>theme</strong></td>
<td valign="top"><a href="#theme">Theme</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RemoveWatchersFromWorkItemResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>workItem</strong></td>
<td valign="top"><a href="#workitem">WorkItem</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RemoveWorkItemsFromThemeResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>theme</strong></td>
<td valign="top"><a href="#theme">Theme</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Space

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>labels</strong></td>
<td valign="top">[<a href="#label">Label</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>statuses</strong></td>
<td valign="top">[<a href="#status">Status</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Status

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#statustype">StatusType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>default</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Theme

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>number</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>actor</strong></td>
<td valign="top"><a href="#actor">Actor</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

The description of a theme as a markdown-formatted string

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sort</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Sort is a string that determines where in a particular horizon column a theme will appear

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>horizon</strong></td>
<td valign="top"><a href="#themehorizon">ThemeHorizon</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>workItems</strong></td>
<td valign="top">[<a href="#workitem">WorkItem</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>comments</strong></td>
<td valign="top">[<a href="#comment">Comment</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>watchers</strong></td>
<td valign="top">[<a href="#user">User</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ThemesQueryResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>themes</strong></td>
<td valign="top">[<a href="#theme">Theme</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cursor</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

An opaque string used for paging. Pass this string to the themes query to iterate through the results a page at a time

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>hasMore</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td>

Indicates if more results are available (by requerying themes, passing the cursor)

</td>
</tr>
</tbody>
</table>

### User

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>username</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>avatar</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### WorkItem

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>number</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>actor</strong></td>
<td valign="top"><a href="#actor">Actor</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

The description of a work item as a markdown-formatted string

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#status">Status</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sort</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Sort is a string that determines where in a particular status column a work item will appear

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>members</strong></td>
<td valign="top">[<a href="#user">User</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>watchers</strong></td>
<td valign="top">[<a href="#user">User</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>labels</strong></td>
<td valign="top">[<a href="#label">Label</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>comments</strong></td>
<td valign="top">[<a href="#comment">Comment</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>effort</strong></td>
<td valign="top"><a href="#effortsize">EffortSize</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>impact</strong></td>
<td valign="top"><a href="#impactsize">ImpactSize</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#date">Date</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### WorkItemsQueryResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>workItems</strong></td>
<td valign="top">[<a href="#workitem">WorkItem</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cursor</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

An opaque string used for paging. Pass this string to the workItems query to iterate through the results a page at a time

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>hasMore</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td>

Indicates if more results are available (by requerying workItems, passing the cursor)

</td>
</tr>
</tbody>
</table>

## Inputs

### AddLabelsToWorkItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>labelIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### AddMembersToWorkItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>memberIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### AddWatchersToThemeInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>watcherIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### AddWatchersToWorkItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>watcherIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### AddWorkItemsToThemeInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>workItemIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateCommentOnThemeInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>body</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>threadId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

When creating a new comment thread, omit this property. Provide this property to add to an existing thread

</td>
</tr>
</tbody>
</table>

### CreateCommentOnWorkItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>body</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>threadId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

When creating a new comment thread, omit this property. Provide this property to add to an existing thread

</td>
</tr>
</tbody>
</table>

### CreateThemeInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>spaceId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sort</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

The sort order of the [Theme](#theme). Omitting this parameter will make the theme the first theme in the horizon column

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

The [Theme](#theme) object's description as a markdown-formatted string

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>horizon</strong></td>
<td valign="top"><a href="#themehorizon">ThemeHorizon</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>workItemIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>watcherIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### CreateWorkItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

The [WorkItem](#workitem) object's description as a markdown-formatted string

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>statusId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sort</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

The sort order of the [WorkItem](#workitem). Omitting this parameter will make the work item the first work item in the status column

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>memberIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>watcherIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>labelIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>effort</strong></td>
<td valign="top"><a href="#effortsize">EffortSize</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>impact</strong></td>
<td valign="top"><a href="#impactsize">ImpactSize</a></td>
<td></td>
</tr>
</tbody>
</table>

### EditCommentInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>body</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### EditThemeInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

The [Theme](#theme) object's description as a markdown-formatted string

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>horizon</strong></td>
<td valign="top"><a href="#themehorizon">ThemeHorizon</a></td>
<td></td>
</tr>
</tbody>
</table>

### EditWorkItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

The [WorkItem](#workitem) object's description as a markdown-formatted string

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>statusId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sort</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>effort</strong></td>
<td valign="top"><a href="#effortsize">EffortSize</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>impact</strong></td>
<td valign="top"><a href="#impactsize">ImpactSize</a></td>
<td></td>
</tr>
</tbody>
</table>

### RemoveLabelsFromWorkItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>labelIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### RemoveMembersFromWorkItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>memberIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### RemoveWatchersFromThemeInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>watcherIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### RemoveWatchersFromWorkItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>watcherIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### RemoveWorkItemsFromThemeInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>workItemIds</strong></td>
<td valign="top">[<a href="#id">ID</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

## Enums

### CacheControlScope

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>PUBLIC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PRIVATE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### EffortSize

T-shirt sizing for effort

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>SMALL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MEDIUM</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LARGE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ImpactSize

T-shirt sizing for impact

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>SMALL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MEDIUM</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LARGE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### IntegrationType

Different types of integrations, mainly useful for when fetching and displaying [Integration](#integration) and [IntegrationUser](#integrationuser) objects

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>GITHUB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FIGMA</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TRELLO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SLACK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DISCORD</strong></td>
<td></td>
</tr>
</tbody>
</table>

### StatusType

Statuses for [WorkItem](#workitem) objects fall into a few different categories

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>BACKLOG</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TODO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IN_PROGRESS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DONE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ARCHIVED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ThemeHorizon

The fixed set of time horizons for [Theme](#theme) objects

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NOW</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NEXT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LATER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ARCHIVED</strong></td>
<td></td>
</tr>
</tbody>
</table>

## Scalars

### Boolean

The `Boolean` scalar type represents `true` or `false`.

### Date

Date custom scalar type

### ID

The `ID` scalar type represents a unique identifier, often used to refetch an object or as key for a cache. The ID type appears in a JSON response as a String; however, it is not intended to be human-readable. When expected as an input type, any string (such as `"4"`) or integer (such as `4`) input value will be accepted as an ID.

### Int

The `Int` scalar type represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1.

### String

The `String` scalar type represents textual data, represented as UTF-8 character sequences. The String type is most often used by GraphQL to represent free-form human-readable text.

### Upload

The `Upload` scalar type represents a file upload.

