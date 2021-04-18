---
title: Elemento Argument
description: O elemento Argument contém uma parte de uma cadeia de caracteres de condição.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- Elemento Argument Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c4adc0b853054d448bc9955f3bd8c64115ac2ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813390"
---
# <a name="argument-element"></a><span data-ttu-id="2214c-104">Elemento Argument</span><span class="sxs-lookup"><span data-stu-id="2214c-104">argument Element</span></span>

<span data-ttu-id="2214c-105">O elemento **Argument** contém uma parte de uma cadeia de caracteres de condição.</span><span class="sxs-lookup"><span data-stu-id="2214c-105">The **argument** element contains one portion of a condition string.</span></span> <span data-ttu-id="2214c-106">Uma cadeia de caracteres de condição normalmente tem uma parte de condição e uma parte de valor.</span><span class="sxs-lookup"><span data-stu-id="2214c-106">A condition string typically has a condition portion and a value portion.</span></span> <span data-ttu-id="2214c-107">Por exemplo, na cadeia de caracteres de condição "artista é igual a Joe", a parte da condição é "Equals" e a parte do valor é "Joe".</span><span class="sxs-lookup"><span data-stu-id="2214c-107">For example, in the condition string "Artist Equals Joe", the condition portion is "Equals" and the value portion is "Joe".</span></span>

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a><span data-ttu-id="2214c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2214c-108">Attributes</span></span>

<span data-ttu-id="2214c-109">**nome** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="2214c-109">**name** (required)</span></span>

<span data-ttu-id="2214c-110">O nome de uma parte da cadeia de caracteres da condição.</span><span class="sxs-lookup"><span data-stu-id="2214c-110">The name of one portion of the condition string.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="2214c-111">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="2214c-111">Parent/Child Elements</span></span>



| <span data-ttu-id="2214c-112">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="2214c-112">Hierarchy</span></span> | <span data-ttu-id="2214c-113">Elementos</span><span class="sxs-lookup"><span data-stu-id="2214c-113">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="2214c-114">Pai</span><span class="sxs-lookup"><span data-stu-id="2214c-114">Parent</span></span>    | [<span data-ttu-id="2214c-115">fragmento</span><span class="sxs-lookup"><span data-stu-id="2214c-115">fragment</span></span>](fragment-element.md) |
| <span data-ttu-id="2214c-116">Filho</span><span class="sxs-lookup"><span data-stu-id="2214c-116">Child</span></span>     | <span data-ttu-id="2214c-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2214c-117">None</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="2214c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2214c-118">Remarks</span></span>

<span data-ttu-id="2214c-119">Quando o atributo **Name** de um elemento **Fragment** é uma característica de item de mídia, como o artista do álbum, ou o gênero, o elemento **Fragment** deve conter dois elementos **Argument** : um que especifica uma condição e outro que especifica um valor.</span><span class="sxs-lookup"><span data-stu-id="2214c-119">When the **name** attribute of a **fragment** element is a media item characteristic such as Album Artist, or Genre, the **fragment** element must contain two **argument** elements: one that specifies a condition and another that specifies a value.</span></span> <span data-ttu-id="2214c-120">A tabela a seguir mostra dois valores possíveis para o atributo **Name** e como os elementos **Argument** são usados para especificar condições e valores.</span><span class="sxs-lookup"><span data-stu-id="2214c-120">The following table shows two possible values for the **name** attribute and how **argument** elements are used to specify conditions and values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2214c-121">Valor do atributo</span><span class="sxs-lookup"><span data-stu-id="2214c-121">Attribute value</span></span></th>
<th><span data-ttu-id="2214c-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="2214c-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2214c-123">Condição</span><span class="sxs-lookup"><span data-stu-id="2214c-123">Condition</span></span></td>
<td><span data-ttu-id="2214c-124">O conteúdo do elemento <strong>Argument</strong> é a parte da condição de uma cadeia de caracteres de condição.</span><span class="sxs-lookup"><span data-stu-id="2214c-124">The content of the <strong>argument</strong> element is the condition portion of a condition string.</span></span> <span data-ttu-id="2214c-125">Por exemplo, no artista de cadeia de caracteres de condição &quot; igual a Joe &quot; , a parte da condição é &quot; igual a &quot; .</span><span class="sxs-lookup"><span data-stu-id="2214c-125">For example, in the condition string &quot;Artist Equals Joe&quot;, the condition portion is &quot;Equals&quot;.</span></span> <span data-ttu-id="2214c-126">A parte da condição de uma cadeia de caracteres de condição deve ser uma das seguintes: Equals, não é igual a, Contains, não contém, é menor que, é maior que, is, is, is, is, is before, é mais recente do que, no máximo, é necessário, no mínimo, o que é.</span><span class="sxs-lookup"><span data-stu-id="2214c-126">The condition portion of a condition string must be one of the following: Equals, Does Not Equal, Contains, Does Not Contain, Is Less Than, Is Greater Than, Is, Is Not, Is Before, Is Later Than, Is More Recent Than, Above, Below, Ascending, Descending, Random, Is At Least, Is No More Than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2214c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2214c-127">Value</span></span></td>
<td><span data-ttu-id="2214c-128">O conteúdo do elemento <strong>Argument</strong> é a parte de valor de uma cadeia de caracteres de condição.</span><span class="sxs-lookup"><span data-stu-id="2214c-128">The content of the <strong>argument</strong> element is the value portion of a condition string.</span></span> <span data-ttu-id="2214c-129">Por exemplo, no artista de cadeia de caracteres de condição &quot; igual a Joe &quot; , a parte de valor é &quot; Joe &quot; . Exemplo</span><span class="sxs-lookup"><span data-stu-id="2214c-129">For example, in the condition string &quot;Artist Equals Joe&quot;, the value portion is &quot;Joe&quot;.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2214c-130">Quando o atributo de **nome** de um elemento de **fragmento** é "limitar o tamanho total para" ou "limitar duração total a", o elemento de **fragmento** deve conter dois elementos de **argumento** : um que especifique um formato e um que especifique um número.</span><span class="sxs-lookup"><span data-stu-id="2214c-130">When the **name** attribute of a **fragment** element is "Limit Total Size To" or "Limit Total Duration To", the **fragment** element must contain two **argument** elements: one that specifies a format and one that specifies a number.</span></span> <span data-ttu-id="2214c-131">A tabela a seguir mostra dois valores possíveis para o atributo **Name** e como os elementos **Argument** são usados para limitar o tamanho ou a duração de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="2214c-131">The following table shows two possible values for the **name** attribute and how **argument** elements are used to limit the size or duration of a playlist.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2214c-132">Valor do atributo</span><span class="sxs-lookup"><span data-stu-id="2214c-132">Attribute value</span></span></th>
<th><span data-ttu-id="2214c-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="2214c-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2214c-134">Formatar</span><span class="sxs-lookup"><span data-stu-id="2214c-134">Format</span></span></td>
<td><span data-ttu-id="2214c-135">Quando o atributo <strong>Name</strong> do elemento <strong>Fragment</strong> é &quot; limitar o tamanho total a &quot; , o conteúdo do elemento <strong>Argument</strong> deve ser um dos seguintes: kilobytes, megabytes ou gigabytes. quando o atributo <strong>Name</strong> do elemento <strong>Fragment</strong> é &quot; limitar a duração total para &quot; , o conteúdo do elemento <strong>Argument</strong> deve ser um dos seguintes: segundos, minutos, horas ou dias.</span><span class="sxs-lookup"><span data-stu-id="2214c-135">When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Size To&quot;, the content of the <strong>argument</strong> element must be one of the following: Kilobytes, Megabytes, or Gigabytes.When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Duration To&quot;, the content of the <strong>argument</strong> element must be one of the following: Seconds, Minutes, Hours, or Days.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2214c-136">Número</span><span class="sxs-lookup"><span data-stu-id="2214c-136">Number</span></span></td>
<td><span data-ttu-id="2214c-137">O conteúdo do elemento <strong>Argument</strong> é um número que limita o tamanho ou a duração da lista de reprodução. Disso</span><span class="sxs-lookup"><span data-stu-id="2214c-137">The content of the <strong>argument</strong> element is a number that limits the size or duration of the playlist.Examples:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2214c-138">Quando o atributo **Name** de um elemento **Fragment** é "limitar número de itens", o elemento **Fragment** deve conter um elemento **Argument** que especifica o número de itens.</span><span class="sxs-lookup"><span data-stu-id="2214c-138">When the **name** attribute of a **fragment** element is "Limit Number of Items", the **fragment** element must contain one **argument** element that specifies the number of items.</span></span> <span data-ttu-id="2214c-139">A tabela a seguir mostra como usar o valor numérico do atributo **Name** .</span><span class="sxs-lookup"><span data-stu-id="2214c-139">The following table shows how to use the Number value of the **name** attribute.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2214c-140">Valor do atributo</span><span class="sxs-lookup"><span data-stu-id="2214c-140">Attribute value</span></span></th>
<th><span data-ttu-id="2214c-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="2214c-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2214c-142">Número</span><span class="sxs-lookup"><span data-stu-id="2214c-142">Number</span></span></td>
<td><span data-ttu-id="2214c-143">O conteúdo do elemento <strong>Argument</strong> é um número que limita o número de itens em uma lista de reprodução. Exemplo</span><span class="sxs-lookup"><span data-stu-id="2214c-143">The content of the <strong>argument</strong> element is a number that limits the number of items in a playlist.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="2214c-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2214c-144">Requirements</span></span>



| <span data-ttu-id="2214c-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="2214c-145">Requirement</span></span> | <span data-ttu-id="2214c-146">Valor</span><span class="sxs-lookup"><span data-stu-id="2214c-146">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="2214c-147">Versão</span><span class="sxs-lookup"><span data-stu-id="2214c-147">Version</span></span><br/> | <span data-ttu-id="2214c-148">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2214c-148">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2214c-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="2214c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2214c-150">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="2214c-150">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="2214c-151">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="2214c-151">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





