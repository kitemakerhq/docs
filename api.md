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
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>workItems</strong></td>
<td valign="top"><a href="#workitemsqueryresult">WorkItemsQueryResult</a>!</td>
<td></td>
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
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>themes</strong></td>
<td valign="top"><a href="#themesqueryresult">ThemesQueryResult</a>!</td>
<td></td>
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
<td></td>
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
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>externalId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>externalName</strong></td>
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
<td></td>
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
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>hasMore</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
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
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#status">Status</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sort</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
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
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>hasMore</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
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
<td></td>
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
<td></td>
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
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
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
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>statusId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sort</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
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
<td></td>
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
<td></td>
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

