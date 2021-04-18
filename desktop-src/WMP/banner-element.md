---
title: Elemento BANNER
description: O elemento BANNER define uma URL para um arquivo gráfico que será exibido no painel de exibição.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Elemento de faixa Windows Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781277"
---
# <a name="banner-element"></a><span data-ttu-id="ee1f4-104">Elemento BANNER</span><span class="sxs-lookup"><span data-stu-id="ee1f4-104">BANNER Element</span></span>

<span data-ttu-id="ee1f4-105">O elemento **banner** define uma URL para um arquivo gráfico que será exibido no painel de exibição.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-105">The **BANNER** element defines a URL to a graphic file that will appear in the display panel.</span></span>

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a><span data-ttu-id="ee1f4-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="ee1f4-106">Attributes</span></span>

<span data-ttu-id="ee1f4-107">**Href** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="ee1f4-107">**HREF** (required)</span></span>

<span data-ttu-id="ee1f4-108">URL para um arquivo gráfico que é exibido no painel de exibição.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-108">URL to a graphic file that is displayed in the display panel.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="ee1f4-109">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="ee1f4-109">Parent/Child Elements</span></span>



| <span data-ttu-id="ee1f4-110">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="ee1f4-110">Hierarchy</span></span>       | <span data-ttu-id="ee1f4-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="ee1f4-111">Elements</span></span>                   |
|-----------------|----------------------------|
| <span data-ttu-id="ee1f4-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ee1f4-112">Parent elements</span></span> | <span data-ttu-id="ee1f4-113">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="ee1f4-113">**ASX**, **ENTRY**</span></span>         |
| <span data-ttu-id="ee1f4-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ee1f4-114">Child elements</span></span>  | <span data-ttu-id="ee1f4-115">**abstract**, **moreinfo**</span><span class="sxs-lookup"><span data-stu-id="ee1f4-115">**ABSTRACT**, **MOREINFO**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ee1f4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee1f4-116">Remarks</span></span>

<span data-ttu-id="ee1f4-117">Esse elemento define uma URL para um arquivo gráfico que aparece no painel de exibição do Windows Media Player, sob o conteúdo do vídeo.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-117">This element defines a URL to a graphic file that appears in the Windows Media Player display panel, beneath the video content.</span></span> <span data-ttu-id="ee1f4-118">Se a mídia for somente áudio, o gráfico de faixa será exibido por si só.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-118">If the media is audio only, the banner graphic is displayed by itself.</span></span> <span data-ttu-id="ee1f4-119">O Windows Media Player reserva um espaço de 32 pixels de altura por 194 pixels de largura (a barra de faixa) para o gráfico.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-119">Windows Media Player reserves a space 32 pixels high by 194 pixels wide (the banner bar) for the graphic.</span></span> <span data-ttu-id="ee1f4-120">Se o gráfico definido na URL for menor que isso, ele será exibido em seu tamanho original.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-120">If the graphic defined in the URL is smaller than that, it displays at its original size.</span></span> <span data-ttu-id="ee1f4-121">Se o elemento gráfico for maior do que o espaço reservado, o Windows Media Player cortará a imagem para se ajustar ao espaço.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-121">If the graphic is larger than the reserved space, Windows Media Player will crop the image to fit the space.</span></span>

<span data-ttu-id="ee1f4-122">Você pode usar um elemento **abstract** dentro do escopo do elemento **banner** para exibir o texto como uma dica de ferramenta quando o usuário pausa o ponteiro do mouse sobre o gráfico de faixa.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-122">You can use an **ABSTRACT** element within the scope of the **BANNER** element to display text as a ToolTip when the user pauses the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="ee1f4-123">Um elemento **moreinfo** dentro de um elemento **banner** define uma URL para a qual o usuário é levado quando o usuário clica no gráfico de faixa.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-123">A **MOREINFO** element within a **BANNER** element defines a URL to which the user is taken when the user clicks the banner graphic.</span></span> <span data-ttu-id="ee1f4-124">(A URL pode ser qualquer caminho ou protocolo, como um link de email, uma URL de protocolo HTTP para um site ou até mesmo um comando do Microsoft JScript.) Quando o ponteiro é movido sobre o gráfico, o gráfico torna-se relevo e parece um botão.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-124">(The URL can be any path or protocol, such as an email link, a Hypertext Transfer Protocol (HTTP) URL to a website, or even a Microsoft JScript command.) When the pointer is moved over the graphic, the graphic becomes embossed and looks like a button.</span></span>

<span data-ttu-id="ee1f4-125">Um elemento de **faixa** definido para um elemento **ASX** é exibido enquanto todos os clipes na playlist estão sendo reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-125">A **BANNER** element defined for an **ASX** element displays while all clips in the playlist are playing.</span></span> <span data-ttu-id="ee1f4-126">Um elemento de **faixa** definido em um elemento de **entrada** é exibido somente enquanto o clipe está sendo reproduzido e, durante esse tempo, substitui qualquer faixa definida dentro do elemento pai **ASX** .</span><span class="sxs-lookup"><span data-stu-id="ee1f4-126">A **BANNER** element defined in an **ENTRY** element displays only while that clip is playing, and during that time overrides any banner defined within the parent **ASX** element.</span></span> <span data-ttu-id="ee1f4-127">Você pode especificar como o player de mídia do Windows reserva espaço para a faixa definindo o atributo **BANNERBAR** do elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="ee1f4-127">You can specify how Windows Media Player reserves space for the banner by setting the **BANNERBAR** attribute of the **ASX** element.</span></span>

<span data-ttu-id="ee1f4-128">Não há suporte para imagens de banner com arquivos DRM ou quando o Windows Media Player está inserido em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="ee1f4-128">Banner images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

## <a name="examples"></a><span data-ttu-id="ee1f4-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ee1f4-129">Examples</span></span>

<span data-ttu-id="ee1f4-130">Este é um exemplo de um elemento de **faixa** sem elementos filho:</span><span class="sxs-lookup"><span data-stu-id="ee1f4-130">The following is an example of a **BANNER** element without child elements:</span></span>


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



<span data-ttu-id="ee1f4-131">Veja a seguir um exemplo de um elemento de **faixa** que contém elementos **abstract** e **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="ee1f4-131">The following is an example of a **BANNER** element containing **ABSTRACT** and **MOREINFO** elements.</span></span>


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a><span data-ttu-id="ee1f4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee1f4-132">Requirements</span></span>



| <span data-ttu-id="ee1f4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee1f4-133">Requirement</span></span> | <span data-ttu-id="ee1f4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ee1f4-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ee1f4-135">Versão</span><span class="sxs-lookup"><span data-stu-id="ee1f4-135">Version</span></span><br/> | <span data-ttu-id="ee1f4-136">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ee1f4-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee1f4-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee1f4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1f4-138">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ee1f4-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="ee1f4-139">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ee1f4-139">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





