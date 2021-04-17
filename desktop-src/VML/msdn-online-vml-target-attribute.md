---
title: Atributo de destino VML
description: Atributo de destino VML
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105759591"
---
# <a name="vml-target-attribute"></a><span data-ttu-id="55c1d-103">Atributo de destino VML</span><span class="sxs-lookup"><span data-stu-id="55c1d-103">VML Target Attribute</span></span>

<span data-ttu-id="55c1d-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="55c1d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="55c1d-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="55c1d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="55c1d-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="55c1d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="55c1d-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="55c1d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="55c1d-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="55c1d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="55c1d-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="55c1d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="55c1d-110">Define um quadro ou uma janela em que uma URL é exibida.</span><span class="sxs-lookup"><span data-stu-id="55c1d-110">Defines a frame or window that a URL is displayed in.</span></span> <span data-ttu-id="55c1d-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="55c1d-111">Read/write.</span></span> <span data-ttu-id="55c1d-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="55c1d-112">**String**.</span></span>

<span data-ttu-id="55c1d-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="55c1d-113">**Applies To**</span></span>

[<span data-ttu-id="55c1d-114">Forma</span><span class="sxs-lookup"><span data-stu-id="55c1d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="55c1d-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="55c1d-115">**Tag Syntax**</span></span>

<span data-ttu-id="55c1d-116"><v: *Element* Target = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="55c1d-116"><v: *element* target=" *expression* "></span></span>

<span data-ttu-id="55c1d-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="55c1d-117">**Remarks**</span></span>

<span data-ttu-id="55c1d-118">O atributo de **destino** é semelhante ao atributo de **destino** HTML padrão de âncoras.</span><span class="sxs-lookup"><span data-stu-id="55c1d-118">The **Target** attribute is similar to the standard HTML **Target** attribute of anchors.</span></span>

<span data-ttu-id="55c1d-119">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="55c1d-119">Values include:</span></span>



| <span data-ttu-id="55c1d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="55c1d-120">Value</span></span>      | <span data-ttu-id="55c1d-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="55c1d-121">Description</span></span>                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55c1d-122">TargetName</span><span class="sxs-lookup"><span data-stu-id="55c1d-122">TargetName</span></span> | <span data-ttu-id="55c1d-123">Cadeia de caracteres que contém o nome do quadro ou da janela na qual carregar o documento.</span><span class="sxs-lookup"><span data-stu-id="55c1d-123">String containing the name of the frame or window in which to load the document.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="55c1d-124">\_ficará</span><span class="sxs-lookup"><span data-stu-id="55c1d-124">\_blank</span></span>    | <span data-ttu-id="55c1d-125">Especifica que o documento vinculado é carregado em uma nova janela em branco.</span><span class="sxs-lookup"><span data-stu-id="55c1d-125">Specifies that the linked document is loaded into a new blank window.</span></span> <span data-ttu-id="55c1d-126">Esta janela não é nomeada.</span><span class="sxs-lookup"><span data-stu-id="55c1d-126">This window is not named.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="55c1d-127">\_meio</span><span class="sxs-lookup"><span data-stu-id="55c1d-127">\_media</span></span>    | <span data-ttu-id="55c1d-128">A partir do Internet Explorer 6 para Windows XP Service Pack 2, o \_ atributo de mídia é obsoleto e não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="55c1d-128">As of Internet Explorer 6 for Windows XP Service Pack 2, the \_media attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="55c1d-129">Primeiro, disponível no Internet Explorer 6, esse valor especificou que o documento vinculado deve ser carregado na barra de mídia.</span><span class="sxs-lookup"><span data-stu-id="55c1d-129">First available in Internet Explorer 6, this value specified that the linked document should be loaded into the Media Bar.</span></span>                |
| <span data-ttu-id="55c1d-130">\_primária</span><span class="sxs-lookup"><span data-stu-id="55c1d-130">\_parent</span></span>   | <span data-ttu-id="55c1d-131">Especifica que o documento vinculado é carregado no pai imediato do documento que contém o link.</span><span class="sxs-lookup"><span data-stu-id="55c1d-131">Specifies that the linked document is loaded into the immediate parent of the document containing the link.</span></span>                                                                                                                                                      |
| <span data-ttu-id="55c1d-132">\_procurando</span><span class="sxs-lookup"><span data-stu-id="55c1d-132">\_search</span></span>   | <span data-ttu-id="55c1d-133">A partir do Internet Explorer 7 para Windows XP Service Pack 2,: o \_ atributo de pesquisa é obsoleto e não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="55c1d-133">As of Internet Explorer 7 for Windows XP Service Pack 2, : The \_search attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="55c1d-134">Primeiro, disponível no Internet Explorer 6, esse valor especificou que o documento vinculado foi carregado no painel de pesquisa do navegador.</span><span class="sxs-lookup"><span data-stu-id="55c1d-134">First available in Internet Explorer 6, this value specified that the linked document was to be loaded into the browser's search pane.</span></span> |
| <span data-ttu-id="55c1d-135">\_auto-restauração</span><span class="sxs-lookup"><span data-stu-id="55c1d-135">\_self</span></span>     | <span data-ttu-id="55c1d-136">Especifica que o documento vinculado é carregado na janela em que o link foi clicado (a janela ativa).</span><span class="sxs-lookup"><span data-stu-id="55c1d-136">Specifies that the linked document is loaded into the window in which the link was clicked (the active window).</span></span>                                                                                                                                                  |
| <span data-ttu-id="55c1d-137">\_Início</span><span class="sxs-lookup"><span data-stu-id="55c1d-137">\_top</span></span>      | <span data-ttu-id="55c1d-138">Especifica que o documento vinculado é carregado na janela mais alta.</span><span class="sxs-lookup"><span data-stu-id="55c1d-138">Specifies that the linked document is loaded into the topmost window.</span></span>                                                                                                                                                                                            |



 

<span data-ttu-id="55c1d-139">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="55c1d-139">*VML Standard Attribute*</span></span>

<span data-ttu-id="55c1d-140">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="55c1d-140">**Example**</span></span>

<span data-ttu-id="55c1d-141">Quando o retângulo é clicado, o navegador carrega o home page da Microsoft Corporation na mesma janela.</span><span class="sxs-lookup"><span data-stu-id="55c1d-141">When the rectangle is clicked, the browser loads the Microsoft Corporation home page in the same window.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="55c1d-142">[Exemplo de atributo de destino](/previous-versions/bb264096(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55c1d-142">[Target Attribute Example](/previous-versions/bb264096(v=vs.85)).</span></span> <span data-ttu-id="55c1d-143">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="55c1d-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 