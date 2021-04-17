---
title: Elemento ENTRY
description: O elemento ENTRY especifica um arquivo de mídia do Windows para renderizar como um clipe.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Elemento de entrada Windows Media Player
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758215"
---
# <a name="entry-element"></a><span data-ttu-id="ecfd9-104">Elemento ENTRY</span><span class="sxs-lookup"><span data-stu-id="ecfd9-104">ENTRY Element</span></span>

<span data-ttu-id="ecfd9-105">O elemento **entry** especifica um arquivo de mídia do Windows para renderizar como um clipe.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-105">The **ENTRY** element specifies a Windows Media file to render as a clip.</span></span>

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a><span data-ttu-id="ecfd9-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="ecfd9-106">Attributes</span></span>

<span data-ttu-id="ecfd9-107">**CLIENTSKIP**</span><span class="sxs-lookup"><span data-stu-id="ecfd9-107">**CLIENTSKIP**</span></span>

<span data-ttu-id="ecfd9-108">Valor que indica se o usuário pode pular para a frente do clipe.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-108">Value indicating whether the user can skip forward past the clip.</span></span>

<span data-ttu-id="ecfd9-109">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-109">Possible values include the following.</span></span>



| <span data-ttu-id="ecfd9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ecfd9-110">Value</span></span> | <span data-ttu-id="ecfd9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ecfd9-111">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="ecfd9-112">YES</span><span class="sxs-lookup"><span data-stu-id="ecfd9-112">YES</span></span>   | <span data-ttu-id="ecfd9-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-113">Default.</span></span> <span data-ttu-id="ecfd9-114">O usuário pode pular o clipe para frente.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-114">User can skip forward past the clip.</span></span> |
| <span data-ttu-id="ecfd9-115">Não</span><span class="sxs-lookup"><span data-stu-id="ecfd9-115">NO</span></span>    | <span data-ttu-id="ecfd9-116">O usuário não pode pular o clipe para frente.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-116">User cannot skip forward past the clip.</span></span>       |



 

<span data-ttu-id="ecfd9-117">**SKIPIFREF**</span><span class="sxs-lookup"><span data-stu-id="ecfd9-117">**SKIPIFREF**</span></span>

<span data-ttu-id="ecfd9-118">Valor que indica se o Windows Media Player deve ignorar esse clipe quando o elemento de **entrada** é incluído em um segundo metarquivo por meio do uso de um elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="ecfd9-118">Value indicating whether Windows Media Player should skip this clip when the **ENTRY** element is included in a second metafile through the use of an **ENTRYREF** element.</span></span>

<span data-ttu-id="ecfd9-119">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-119">Possible values include the following.</span></span>



| <span data-ttu-id="ecfd9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ecfd9-120">Value</span></span> | <span data-ttu-id="ecfd9-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="ecfd9-121">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfd9-122">YES</span><span class="sxs-lookup"><span data-stu-id="ecfd9-122">YES</span></span>   | <span data-ttu-id="ecfd9-123">O Windows Media Player irá ignorar essa entrada, se for referenciada por meio de um elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="ecfd9-123">Windows Media Player will ignore this entry, if referenced through an **ENTRYREF** element.</span></span> |
| <span data-ttu-id="ecfd9-124">Não</span><span class="sxs-lookup"><span data-stu-id="ecfd9-124">NO</span></span>    | <span data-ttu-id="ecfd9-125">Padrão.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-125">Default.</span></span> <span data-ttu-id="ecfd9-126">O Windows Media Player não ignorará essa entrada.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-126">Windows Media Player will not ignore this entry.</span></span>                                   |



 

## <a name="parentchild-elements"></a><span data-ttu-id="ecfd9-127">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="ecfd9-127">Parent/Child Elements</span></span>



| <span data-ttu-id="ecfd9-128">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="ecfd9-128">Hierarchy</span></span>       | <span data-ttu-id="ecfd9-129">Elementos</span><span class="sxs-lookup"><span data-stu-id="ecfd9-129">Elements</span></span>                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfd9-130">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ecfd9-130">Parent elements</span></span> | <span data-ttu-id="ecfd9-131">**ASX**, **evento**, **repetir**</span><span class="sxs-lookup"><span data-stu-id="ecfd9-131">**ASX**, **EVENT**, **REPEAT**</span></span>                                                                                                                                                               |
| <span data-ttu-id="ecfd9-132">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ecfd9-132">Child elements</span></span>  | <span data-ttu-id="ecfd9-133">**abstrato**, **autor**, **faixa**, **base**, **direitos autorais**,  **duração**, **moreinfo**, **param**, **PREVIEWDURATION**, **ref**, **STARTMARKER**, **StartTime**, **title**</span><span class="sxs-lookup"><span data-stu-id="ecfd9-133">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **DURATION**, **ENDMARKER**, **MOREINFO**, **PARAM**, **PREVIEWDURATION**, **REF**, **STARTMARKER**, **STARTTIME**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ecfd9-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecfd9-134">Remarks</span></span>

<span data-ttu-id="ecfd9-135">Esse elemento é a construção fundamental em um metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-135">This element is the fundamental construct in a Windows Media metafile.</span></span> <span data-ttu-id="ecfd9-136">O elemento **entry** e seus atributos associados definem meta-informações para uma única parte lógica de conteúdo, chamada de clipe.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-136">The **ENTRY** element and its associated attributes define meta-information for a single, logical piece of content, called a clip.</span></span> <span data-ttu-id="ecfd9-137">Elementos filho dentro do escopo de um elemento de **entrada** definem o conteúdo de mídia para o Windows Media Player abrir (**ref**), informações sobre o clipe que o Windows Media Player exibirá como texto (**autor**, **direitos autorais**, **título**) e outras configurações relacionadas ao clipe.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-137">Child elements within the scope of an **ENTRY** element define media content for Windows Media Player to open (**REF**), information about the clip that Windows Media Player will display as text (**AUTHOR**, **COPYRIGHT**, **TITLE**), and other settings related to the clip.</span></span> <span data-ttu-id="ecfd9-138">O elemento filho **ref** vincula o conteúdo a ser transmitido para o elemento de **entrada** pai.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-138">The **REF** child element links the content to be streamed for the parent **ENTRY** element.</span></span> <span data-ttu-id="ecfd9-139">Embora o script não seja interrompido, a **entrada** não faz sentido sem um filho de **referência** .</span><span class="sxs-lookup"><span data-stu-id="ecfd9-139">Though the script will not break, the **ENTRY** is meaningless without a **REF** child.</span></span>

<span data-ttu-id="ecfd9-140">Se o valor do atributo **CLIENTSKIP** for no, o usuário não poderá pular para frente a parte do conteúdo definido pelo elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="ecfd9-140">If the value of the **CLIENTSKIP** attribute is NO, the user cannot skip forward past the piece of content defined by the **ENTRY** element.</span></span> <span data-ttu-id="ecfd9-141">Isso não funcionará se o elemento de **referência** filho fizer referência a outro metarquivo.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-141">This does not work if the child **REF** element references another metafile.</span></span> <span data-ttu-id="ecfd9-142">Os metaarquivos aninhados devem ser referenciados usando o elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="ecfd9-142">Nested metafiles should be referenced using the **ENTRYREF** element.</span></span>

<span data-ttu-id="ecfd9-143">O atributo **SKIPIFREF** pertence apenas aos elementos de **entrada** que são incluídos em um segundo metarquivo por meio do uso de um elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="ecfd9-143">The **SKIPIFREF** attribute pertains only to **ENTRY** elements that are included in a second metafile through the use of an **ENTRYREF** element.</span></span> <span data-ttu-id="ecfd9-144">O elemento **ENTRYREF** faz referência a outro metarquivo para inclusão lógica no arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-144">The **ENTRYREF** element references another metafile for logical inclusion in the current file.</span></span> <span data-ttu-id="ecfd9-145">Se o valor do atributo **SKIPIFREF** para um elemento de **entrada** do arquivo de METARQUIVO referenciado for sim, o Windows Media Player ignorará essa entrada retirada e passará para o próximo elemento de **entrada** , se houver.</span><span class="sxs-lookup"><span data-stu-id="ecfd9-145">If the value of the **SKIPIFREF** attribute for an **ENTRY** element from the referenced metafile file is YES, Windows Media Player ignores this pulled-in entry, and moves on to the next **ENTRY** element, if any.</span></span> <span data-ttu-id="ecfd9-146">O próximo elemento de **entrada** pode ser a entrada seguinte no arquivo original ou a entrada seguinte no metarquivo referenciado no elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="ecfd9-146">The next **ENTRY** element can be the next entry in the original file, or the next entry in the metafile referenced in the **ENTRYREF** element.</span></span>

## <a name="examples"></a><span data-ttu-id="ecfd9-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ecfd9-147">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="ecfd9-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecfd9-148">Requirements</span></span>



| <span data-ttu-id="ecfd9-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecfd9-149">Requirement</span></span> | <span data-ttu-id="ecfd9-150">Valor</span><span class="sxs-lookup"><span data-stu-id="ecfd9-150">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="ecfd9-151">Versão</span><span class="sxs-lookup"><span data-stu-id="ecfd9-151">Version</span></span><br/> | <span data-ttu-id="ecfd9-152">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ecfd9-152">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ecfd9-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecfd9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecfd9-154">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ecfd9-154">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="ecfd9-155">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ecfd9-155">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





