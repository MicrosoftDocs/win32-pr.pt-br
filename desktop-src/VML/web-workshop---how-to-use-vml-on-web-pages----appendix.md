---
title: Apêndice (VML)
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Web Workshop, namespaces
- Web Workshop, estilos de comportamento
- Criando páginas da Web, namespaces
- Criando páginas da Web, estilos de comportamento
- Linguagem VML (VML), namespaces
- VML (linguagem VML), namespaces
- gráficos de vetor, namespaces
- Linguagem VML (VML), estilos de comportamento
- VML (linguagem VML), estilos de comportamento
- gráficos vetoriais, estilos de comportamento
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d4e7a6a7e44671b7ee835eea263d9ce36a27d8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369127"
---
# <a name="appendix-vml"></a><span data-ttu-id="c0abc-114">Apêndice (VML)</span><span class="sxs-lookup"><span data-stu-id="c0abc-114">Appendix (VML)</span></span>

<span data-ttu-id="c0abc-115">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c0abc-115">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c0abc-116">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="c0abc-116">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c0abc-117">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="c0abc-117">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c0abc-118">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="c0abc-118">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c0abc-119">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c0abc-119">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c0abc-120">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c0abc-120">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c0abc-121">Para permitir que os navegadores saibam como entregar os dados a um processador específico da VML, você precisa digitar algumas informações, como namespaces e estilos de comportamento.</span><span class="sxs-lookup"><span data-stu-id="c0abc-121">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as namespaces and behavior styles.</span></span> <span data-ttu-id="c0abc-122">Em seguida, você pode usar a VML para digitar elementos gráficos na `<BODY>` região.</span><span class="sxs-lookup"><span data-stu-id="c0abc-122">You can then use VML to type graphics in the `<BODY>` region.</span></span>

<span data-ttu-id="c0abc-123">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="c0abc-123">In this topic:</span></span>

-   [<span data-ttu-id="c0abc-124">Namespaces</span><span class="sxs-lookup"><span data-stu-id="c0abc-124">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="c0abc-125">Estilos de comportamento</span><span class="sxs-lookup"><span data-stu-id="c0abc-125">Behavior Styles</span></span>](#behavior-styles)

## <a name="namespaces"></a><span data-ttu-id="c0abc-126">Namespaces</span><span class="sxs-lookup"><span data-stu-id="c0abc-126">Namespaces</span></span>

<span data-ttu-id="c0abc-127">Um mecanismo XML indica o namespace do qual um elemento é proveniente.</span><span class="sxs-lookup"><span data-stu-id="c0abc-127">An XML mechanism indicates the namespace that an element comes from.</span></span> <span data-ttu-id="c0abc-128">Se você alternar da análise em HTML para analisar em XML, esse mecanismo indicará o comutador em HTML.</span><span class="sxs-lookup"><span data-stu-id="c0abc-128">If you switch from parsing in HTML to parsing in XML, this mechanism indicates the switch within HTML.</span></span>

<span data-ttu-id="c0abc-129">Pergunte ao fornecedor do seu processador VML quais informações são necessárias para o namespace XML.</span><span class="sxs-lookup"><span data-stu-id="c0abc-129">Ask the vender of your VML processor what information is required for the XML namespace.</span></span>

<span data-ttu-id="c0abc-130">Se você usar o Microsoft Internet Explorer para renderizar a VML, sempre digite a seguinte linha na `<HTML>` marca:</span><span class="sxs-lookup"><span data-stu-id="c0abc-130">If you use Microsoft Internet Explorer to render VML, always type the following line in the `<HTML>` tag:</span></span>


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



<span data-ttu-id="c0abc-131">Essas informações dizem ao Internet Explorer para mudar para o namespace "urn: schemas-microsoft-com: VML" ao analisar uma marca XML com um prefixo `v:` e para entregar os dados resultantes para o processador da VML.</span><span class="sxs-lookup"><span data-stu-id="c0abc-131">This information tells Internet Explorer to switch to namespace "urn:schemas-microsoft-com:vml" when parsing an XML tag with a prefix `v:`, and to hand off the resulting data to the VML processor.</span></span>

<span data-ttu-id="c0abc-132">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="c0abc-132">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="behavior-styles"></a><span data-ttu-id="c0abc-133">Estilos de comportamento</span><span class="sxs-lookup"><span data-stu-id="c0abc-133">Behavior Styles</span></span>

<span data-ttu-id="c0abc-134">A VML é definida no Microsoft Internet Explorer como um comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="c0abc-134">VML is defined in Microsoft Internet Explorer as a default behavior.</span></span>

<span data-ttu-id="c0abc-135">Para renderizar a VML, sempre digite as seguintes linhas na `<HEAD>` região:</span><span class="sxs-lookup"><span data-stu-id="c0abc-135">To render VML, always type the following lines in the `<HEAD>` region:</span></span>


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



<span data-ttu-id="c0abc-136">A VML é implementada no Internet Explorer por meio de VGX.DLL.</span><span class="sxs-lookup"><span data-stu-id="c0abc-136">VML is implemented in Internet Explorer through VGX.DLL.</span></span> <span data-ttu-id="c0abc-137">Se a instalação inicial do navegador não incluía o comportamento de VML, talvez seja necessário adicioná-lo como uma opção.</span><span class="sxs-lookup"><span data-stu-id="c0abc-137">If your initial installation of the browser did not include VML behavior, you may need to add it as an option.</span></span> <span data-ttu-id="c0abc-138">Você não precisa adicionar uma `<object>` marca.</span><span class="sxs-lookup"><span data-stu-id="c0abc-138">You do not need to add an `<object>` tag.</span></span>

 

 
