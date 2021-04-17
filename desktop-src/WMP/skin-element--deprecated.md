---
title: Elemento SKIN (preterido)
description: Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Elemento SKIN (preterido) Windows Media Player
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811243"
---
# <a name="skin-element-deprecated"></a><span data-ttu-id="34ba2-104">Elemento SKIN (preterido)</span><span class="sxs-lookup"><span data-stu-id="34ba2-104">SKIN Element (deprecated)</span></span>

<span data-ttu-id="34ba2-105">Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="34ba2-105">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="34ba2-106">O elemento **Skin** especifica uma URL para uma borda.</span><span class="sxs-lookup"><span data-stu-id="34ba2-106">The **SKIN** element specifies a URL to a border.</span></span>

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="34ba2-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="34ba2-107">Attributes</span></span>

<span data-ttu-id="34ba2-108">**Href** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="34ba2-108">**HREF** (required)</span></span>

<span data-ttu-id="34ba2-109">URL para um arquivo de borda compactado com uma extensão de nome de arquivo. wmz.</span><span class="sxs-lookup"><span data-stu-id="34ba2-109">URL for a compressed border file with a file name extension .wmz.</span></span> <span data-ttu-id="34ba2-110">Para o Windows Media Player 9 Series ou posterior, esse valor pode fazer referência somente a arquivos de borda no disco rígido do usuário localizado no mesmo diretório que a playlist de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="34ba2-110">For Windows Media Player 9 Series or later, this value can reference only border files on the user's hard disk located in the same directory as the metafile playlist.</span></span> <span data-ttu-id="34ba2-111">Consulte o código de exemplo.</span><span class="sxs-lookup"><span data-stu-id="34ba2-111">See the example code.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="34ba2-112">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="34ba2-112">Parent/Child Elements</span></span>



| <span data-ttu-id="34ba2-113">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="34ba2-113">Hierarchy</span></span>       | <span data-ttu-id="34ba2-114">Elementos</span><span class="sxs-lookup"><span data-stu-id="34ba2-114">Elements</span></span> |
|-----------------|----------|
| <span data-ttu-id="34ba2-115">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="34ba2-115">Parent elements</span></span> | <span data-ttu-id="34ba2-116">**ASX**</span><span class="sxs-lookup"><span data-stu-id="34ba2-116">**ASX**</span></span>  |
| <span data-ttu-id="34ba2-117">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="34ba2-117">Child elements</span></span>  | <span data-ttu-id="34ba2-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="34ba2-118">None</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="34ba2-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="34ba2-119">Remarks</span></span>

<span data-ttu-id="34ba2-120">O elemento **Skin** é usado para criar uma borda, que é semelhante a uma capa, mas é exibido na área em **execução** do modo completo do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="34ba2-120">The **SKIN** element is used to create a border, which is similar to a skin but is displayed in the **Now Playing** area of the full mode Windows Media Player.</span></span> <span data-ttu-id="34ba2-121">O elemento **Skin** é usado apenas para bordas, que aparecem dentro do modo completo do Windows Media Player e não para capas regulares, que substituem totalmente o Windows Media Player do modo compacto.</span><span class="sxs-lookup"><span data-stu-id="34ba2-121">The **SKIN** element is used only for borders, which appear inside the full mode Windows Media Player, and not for regular skins, which entirely replace the compact mode Windows Media Player.</span></span>

<span data-ttu-id="34ba2-122">Em um pacote de download do Windows Media (com uma extensão de nome de arquivo. WMD), o elemento **Skin** permite que uma borda tenha conteúdo e seja vinculada a outros sites.</span><span class="sxs-lookup"><span data-stu-id="34ba2-122">In a Windows Media Download Package (with a .wmd file name extension), the **SKIN** element enables a border to have content and link to other sites.</span></span> <span data-ttu-id="34ba2-123">O pacote de download do Windows Media é um arquivo compactado que contém um arquivo de borda e um metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="34ba2-123">The Windows Media Download Package is a compressed file that contains a border file and a Windows Media metafile.</span></span> <span data-ttu-id="34ba2-124">O arquivo de borda (com uma extensão de nome de arquivo. wmz) é compactado e inclui um arquivo de definição de capa (com uma extensão de nome de arquivo. WMS).</span><span class="sxs-lookup"><span data-stu-id="34ba2-124">The border file (with a .wmz file name extension) is compressed, and includes a skin definition file (with a .wms file name extension).</span></span>

<span data-ttu-id="34ba2-125">Um elemento **Skin** tem três componentes:</span><span class="sxs-lookup"><span data-stu-id="34ba2-125">A **SKIN** element has three components:</span></span>

-   <span data-ttu-id="34ba2-126">Uma capa</span><span class="sxs-lookup"><span data-stu-id="34ba2-126">A skin</span></span>
-   <span data-ttu-id="34ba2-127">Algum conteúdo</span><span class="sxs-lookup"><span data-stu-id="34ba2-127">Some content</span></span>
-   <span data-ttu-id="34ba2-128">Um metarquivo</span><span class="sxs-lookup"><span data-stu-id="34ba2-128">A metafile</span></span>

<span data-ttu-id="34ba2-129">As capas incluídas nos pacotes de download de mídia do Windows devem ser retangulares em forma.</span><span class="sxs-lookup"><span data-stu-id="34ba2-129">Skins included with Windows Media Download Packages must be rectangular in shape.</span></span> <span data-ttu-id="34ba2-130">A criação de bordas com capas que não são retangulares pode gerar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="34ba2-130">Creating borders with skins that are not rectangular may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="34ba2-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34ba2-131">Examples</span></span>


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a><span data-ttu-id="34ba2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34ba2-132">Requirements</span></span>



| <span data-ttu-id="34ba2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="34ba2-133">Requirement</span></span> | <span data-ttu-id="34ba2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="34ba2-134">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="34ba2-135">Versão</span><span class="sxs-lookup"><span data-stu-id="34ba2-135">Version</span></span><br/> | <span data-ttu-id="34ba2-136">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="34ba2-136">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34ba2-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="34ba2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34ba2-138">**Bordas do Windows Media Player (preterido)**</span><span class="sxs-lookup"><span data-stu-id="34ba2-138">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="34ba2-139">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="34ba2-139">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="34ba2-140">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="34ba2-140">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





