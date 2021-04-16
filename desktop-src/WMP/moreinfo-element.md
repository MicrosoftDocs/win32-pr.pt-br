---
title: Elemento MOREINFO
description: O elemento MOREINFO especifica uma URL para um site, endereço de email ou comando de script associado a um show, clip ou banner.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Elemento MOREINFO do Windows Media Player
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efc54fe9745566ec7eaa87b7f0f4645b07a055f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772970"
---
# <a name="moreinfo-element"></a><span data-ttu-id="7e6f8-104">Elemento MOREINFO</span><span class="sxs-lookup"><span data-stu-id="7e6f8-104">MOREINFO Element</span></span>

<span data-ttu-id="7e6f8-105">O elemento **moreinfo** especifica uma URL para um site, endereço de email ou comando de script associado a um show, clip ou banner.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-105">The **MOREINFO** element specifies a URL to a website, email address, or script command associated with a show, clip, or banner.</span></span>

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a><span data-ttu-id="7e6f8-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="7e6f8-106">Attributes</span></span>

<span data-ttu-id="7e6f8-107">**Href** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="7e6f8-107">**HREF** (required)</span></span>

<span data-ttu-id="7e6f8-108">URL para um site, endereço de email ou comando de script.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-108">URL to a website, email address, or script command.</span></span>

<span data-ttu-id="7e6f8-109">**ALVO**</span><span class="sxs-lookup"><span data-stu-id="7e6f8-109">**TARGET**</span></span>

<span data-ttu-id="7e6f8-110">Valor que define o quadro ou a janela em que o navegador abrirá a página definida pelo atributo **href** .</span><span class="sxs-lookup"><span data-stu-id="7e6f8-110">Value defining the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span>

<span data-ttu-id="7e6f8-111">Pode ser uma cadeia de caracteres que contém um nome de janela ou um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-111">This can be a string containing a window name, or one of the following values.</span></span>



| <span data-ttu-id="7e6f8-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7e6f8-112">Value</span></span>    | <span data-ttu-id="7e6f8-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e6f8-113">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e6f8-114">\_ficará</span><span class="sxs-lookup"><span data-stu-id="7e6f8-114">\_blank</span></span>  | <span data-ttu-id="7e6f8-115">O documento é carregado em uma nova janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-115">The document loads in a new browser window.</span></span>                                                                              |
| <span data-ttu-id="7e6f8-116">\_auto-restauração</span><span class="sxs-lookup"><span data-stu-id="7e6f8-116">\_self</span></span>   | <span data-ttu-id="7e6f8-117">O documento é carregado no mesmo quadro que o documento atual que contém o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-117">The document loads in the same frame as the current document containing the Windows Media Player control.</span></span>                |
| <span data-ttu-id="7e6f8-118">\_primária</span><span class="sxs-lookup"><span data-stu-id="7e6f8-118">\_parent</span></span> | <span data-ttu-id="7e6f8-119">O documento é carregado no quadro pai imediato do quadro atual ou no quadro atual, se não houver quadro pai.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-119">The document loads in the immediate parent frame of the current frame, or the current frame if there is no parent frame.</span></span> |
| <span data-ttu-id="7e6f8-120">\_Início</span><span class="sxs-lookup"><span data-stu-id="7e6f8-120">\_top</span></span>    | <span data-ttu-id="7e6f8-121">O documento é carregado na janela completa do navegador, substituindo todos os outros quadros ou documentos.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-121">The document loads in the full browser window, replacing all other frames or documents.</span></span>                                  |



 

## <a name="parentchild-elements"></a><span data-ttu-id="7e6f8-122">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="7e6f8-122">Parent/Child Elements</span></span>



| <span data-ttu-id="7e6f8-123">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="7e6f8-123">Hierarchy</span></span>       | <span data-ttu-id="7e6f8-124">Elementos</span><span class="sxs-lookup"><span data-stu-id="7e6f8-124">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="7e6f8-125">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7e6f8-125">Parent elements</span></span> | <span data-ttu-id="7e6f8-126">**ASX**, **entrada**, **faixa**</span><span class="sxs-lookup"><span data-stu-id="7e6f8-126">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="7e6f8-127">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7e6f8-127">Child elements</span></span>  | <span data-ttu-id="7e6f8-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7e6f8-128">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="7e6f8-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e6f8-129">Remarks</span></span>

<span data-ttu-id="7e6f8-130">Esse elemento Especifica uma URL para um site, endereço de email **ou comando de script. O usuário pode acessar o destino da URL clicando no gráfico ou no texto associado** ao elemento moreinfo.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-130">This element specifies a URL to a website, email address, **or script command. The user can access the target of the URL by clicking on the graphic or text associated with the MOREINFO** element.</span></span> <span data-ttu-id="7e6f8-131">Os detalhes dependem do elemento pai do elemento **moreinfo** :</span><span class="sxs-lookup"><span data-stu-id="7e6f8-131">The details depend on the parent element of the **MOREINFO** element:</span></span>

-   <span data-ttu-id="7e6f8-132">Se o elemento **moreinfo** for o filho de um elemento **ASX** , o usuário poderá acessar a URL clicando no título mostrar.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-132">If the **MOREINFO** element is the child of an **ASX** element, the user can access the URL by clicking the show title.</span></span>
-   <span data-ttu-id="7e6f8-133">Se o elemento **moreinfo** for o filho de um elemento de **entrada** , o usuário poderá acessar a URL clicando no título do clipe.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-133">If the **MOREINFO** element is the child of an **ENTRY** element, the user can access the URL by clicking the clip title.</span></span>
-   <span data-ttu-id="7e6f8-134">Se o elemento **moreinfo** for o filho de um elemento **banner** , o usuário poderá acessar a URL clicando no gráfico de faixa.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-134">If the **MOREINFO** element is the child of a **BANNER** element, the user can access the URL by clicking the banner graphic.</span></span>

<span data-ttu-id="7e6f8-135">Se o atributo **href** especificar uma URL para um site, o navegador será aberto e navegará até a URL.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-135">If the **HREF** attribute specifies a URL to a website, the browser opens and navigates to the URL.</span></span> <span data-ttu-id="7e6f8-136">Se o atributo **href** especificar um endereço de email, o aplicativo de email do usuário será iniciado.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-136">If the **HREF** attribute specifies an email address, the user's email application starts.</span></span> <span data-ttu-id="7e6f8-137">Se o atributo **href** especificar um comando de script, o comando de script será executado no navegador.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-137">If the **HREF** attribute specifies a script command, the script command executes in the browser.</span></span>

<span data-ttu-id="7e6f8-138">**Observação**</span><span class="sxs-lookup"><span data-stu-id="7e6f8-138">**Note**</span></span>

<span data-ttu-id="7e6f8-139">Se o elemento **moreinfo** aparecer dentro de um elemento **ASX** ou **entry** , quando o cursor do mouse for mantido sobre o título do show (para um elemento **ASX** ) ou um clip (para um elemento de **entrada** ), a URL definida no atributo **href** poderá ser selecionada e acessada pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-139">If the **MOREINFO** element appears within an **ASX** or **ENTRY** element, when the mouse cursor is held over the title of the show (for an **ASX** element) or clip (for an **ENTRY** element), the URL defined in the **HREF** attribute can be selected and accessed by Windows Media Player.</span></span>

<span data-ttu-id="7e6f8-140">O atributo de **destino** define o quadro ou a janela em que o navegador irá abrir a página definida pelo atributo **href** .</span><span class="sxs-lookup"><span data-stu-id="7e6f8-140">The **TARGET** attribute defines the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span> <span data-ttu-id="7e6f8-141">Os valores para esse atributo seguem a sintaxe HTML padrão e as definições.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-141">The values for this attribute follow standard HTML syntax and definitions.</span></span> <span data-ttu-id="7e6f8-142">No caso de um controle inserido em uma página da Web, se nenhum atributo de **destino** for definido, a URL carregará a janela atual do navegador e substituirá a página existente, o que significa que o conteúdo parará de ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-142">In the case of a control embedded in a webpage, if no **TARGET** attribute is defined, the URL loads the current browser window and replaces the existing page, which means the content stops playing.</span></span> <span data-ttu-id="7e6f8-143">Portanto, é recomendável que você sempre especifique um atributo de **destino** ao inserir o controle do Windows Media Player em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-143">Therefore, it is recommended that you always specify a **TARGET** attribute when embedding the Windows Media Player control in a webpage.</span></span>

<span data-ttu-id="7e6f8-144">Se o metarquivo é aberto no Windows Media Player autônomo, o atributo de **destino** é ignorado e a URL é carregada em uma janela de navegador existente.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-144">If the metafile is opened in the stand-alone Windows Media Player, the **TARGET** attribute is ignored, and the URL loads in an existing browser window.</span></span> <span data-ttu-id="7e6f8-145">Se não houver janela do navegador aberta no momento, a URL será carregada em uma nova janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="7e6f8-145">If there is no browser window currently open, the URL loads in a new browser window.</span></span>

## <a name="examples"></a><span data-ttu-id="7e6f8-146">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7e6f8-146">Examples</span></span>


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="7e6f8-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e6f8-147">Requirements</span></span>



| <span data-ttu-id="7e6f8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e6f8-148">Requirement</span></span> | <span data-ttu-id="7e6f8-149">Valor</span><span class="sxs-lookup"><span data-stu-id="7e6f8-149">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="7e6f8-150">Versão</span><span class="sxs-lookup"><span data-stu-id="7e6f8-150">Version</span></span><br/> | <span data-ttu-id="7e6f8-151">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7e6f8-151">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e6f8-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e6f8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e6f8-153">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7e6f8-153">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="7e6f8-154">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7e6f8-154">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





