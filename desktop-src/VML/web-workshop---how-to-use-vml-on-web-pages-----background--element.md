---
title: Usando o elemento background
description: Usando o elemento background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Web Workshop, elemento de plano de fundo
- Criando páginas da Web, elemento de plano de fundo
- Linguagem VML (VML), elemento de plano de fundo
- VML (linguagem VML), elemento de segundo plano
- elementos gráficos vetoriais, elemento background
- elemento background
- Elementos de VML, plano de fundo
- Formas de VML, elemento de plano de fundo
- Linguagem VML (VML), personalizando planos de fundo
- VML (linguagem VML), personalizando planos de fundo
- gráficos vetoriais, personalizando planos de fundo
- Formas de VML, personalizando planos de fundo
- Personalizando planos de fundo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823817"
---
# <a name="using-the-background-element"></a><span data-ttu-id="78407-116">Usando o elemento background</span><span class="sxs-lookup"><span data-stu-id="78407-116">Using the Background Element</span></span>

<span data-ttu-id="78407-117">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="78407-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="78407-118">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="78407-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="78407-119">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="78407-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="78407-120">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="78407-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="78407-121">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="78407-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="78407-122">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="78407-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="78407-123">Neste tópico, Ilustraremos como você pode personalizar o plano de fundo de uma página da Web usando o `<background>` elemento fornecido em VML.</span><span class="sxs-lookup"><span data-stu-id="78407-123">In this topic, we will illustrate how you can customize the background of a Web page by using the `<background>` element provided in VML.</span></span>

<span data-ttu-id="78407-124">Como você aprendeu no tópico [ `<fill>` use](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) , você pode posicionar o `<fill>` subelemento dentro do `<shape>` , `<shapetype>` ou qualquer elemento Shape predefinido para descrever como preencher a forma.</span><span class="sxs-lookup"><span data-stu-id="78407-124">As you've learned from the [Use `<fill>`](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) topic, you can place the `<fill>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span>

<span data-ttu-id="78407-125">Da mesma forma, você pode posicionar o `<fill>` subelemento dentro do `<background>` elemento para descrever como preencher o plano de fundo de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="78407-125">Similarly, you can place the `<fill>` sub-element inside the `<background>` element to describe how to fill the background of a Web page.</span></span> <span data-ttu-id="78407-126">Você pode usar os atributos de Propriedade do `<fill>` subelemento para personalizar o efeito de preenchimento, como [preenchimento gradual](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), preenchimento de [padrão](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)ou preenchimento de [imagem](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span><span class="sxs-lookup"><span data-stu-id="78407-126">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [pattern fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), or [picture fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span></span>

<span data-ttu-id="78407-127">Por exemplo, para desenhar um plano de fundo preenchido com gradiente, você pode digitar as seguintes linhas na `<BODY>` região da sua página da Web:</span><span class="sxs-lookup"><span data-stu-id="78407-127">For example, to draw a gradient-filled background, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





<span data-ttu-id="78407-128">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span><span class="sxs-lookup"><span data-stu-id="78407-128">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span></span>

 

 