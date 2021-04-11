---
title: Introdução à VML
description: Introdução à VML
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Linguagem VML (VML), referência
- VML (linguagem VML), referência
- gráficos vetoriais, referência de VML
- gráficos vetoriais, linguagem VML (VML)
- referência para linguagem VML (VML)
- Referência de VML
- Linguagem VML (VML), elemento Shape
- VML (linguagem VML), elemento Shape
- elementos gráficos vetoriais, elemento Shape
- Elemento Shape
- Elementos de VML, forma
- Linguagem VML (VML), VBScript
- VML (linguagem VML), VBScript
- Linguagem VML (VML), JavaScript
- VML (linguagem VML), JavaScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7a370519e3f173e7418f1aa0510cac768ff46c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366171"
---
# <a name="vml-introduction"></a><span data-ttu-id="af43c-118">Introdução à VML</span><span class="sxs-lookup"><span data-stu-id="af43c-118">VML Introduction</span></span>

<span data-ttu-id="af43c-119">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="af43c-119">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="af43c-120">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="af43c-120">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="af43c-121">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="af43c-121">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="af43c-122">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="af43c-122">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="af43c-123">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="af43c-123">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="af43c-124">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="af43c-124">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="af43c-125">Este documento fornece uma referência detalhada completa para a implementação do linguagem VML (VML) que é enviado com o Microsoft Office 2000.</span><span class="sxs-lookup"><span data-stu-id="af43c-125">This document gives a complete detailed reference to the implementation of the Vector Markup Language (VML) that is shipped with Microsoft Office 2000.</span></span> <span data-ttu-id="af43c-126">Outras implementações podem variar.</span><span class="sxs-lookup"><span data-stu-id="af43c-126">Other implementations may vary.</span></span> <span data-ttu-id="af43c-127">Consulte a [especificação da VML](https://www.w3.org/TR/NOTE-datetime.html) para obter mais informações sobre a VML como padrão.</span><span class="sxs-lookup"><span data-stu-id="af43c-127">Consult the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) for more information about VML as a standard.</span></span>

<span data-ttu-id="af43c-128">A VML é definida como um conjunto de elementos XML e os atributos correspondentes para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="af43c-128">VML is defined as a set of XML elements and the corresponding attributes for each element.</span></span> <span data-ttu-id="af43c-129">Como o elemento **Shape** é o bloco de construção básico de VML, clique [aqui](shape-element--vml.md) para iniciar a referência.</span><span class="sxs-lookup"><span data-stu-id="af43c-129">Since the **Shape** element is the basic building block of VML, click [here](shape-element--vml.md) to begin the reference.</span></span>

<span data-ttu-id="af43c-130">Observe que essa referência contém vários exemplos e demonstrações.</span><span class="sxs-lookup"><span data-stu-id="af43c-130">Note that this reference contains several examples and demos.</span></span> <span data-ttu-id="af43c-131">Você deve ter o Microsoft Internet Explorer 5,0 ou superior instalado para exibir a VML ao vivo.</span><span class="sxs-lookup"><span data-stu-id="af43c-131">You must have Microsoft Internet Explorer 5.0 or greater installed to view the live VML.</span></span>

<span data-ttu-id="af43c-132">Além das informações sobre como usar elementos e atributos como marcas XML que estendem HTML, essa referência contém sintaxe e exemplos que mostram como usar os recursos de script e Modelo de Objeto do Documento do Internet Explorer 5 ou superior.</span><span class="sxs-lookup"><span data-stu-id="af43c-132">In addition to the information about using elements and attributes as XML tags that extend HTML, this reference contains syntax and examples that show how to use the scripting and the Document Object Model features of Internet Explorer 5 or greater.</span></span> <span data-ttu-id="af43c-133">O uso de script com VML permite que você crie elementos "imediatamente" e manipule atributos em tempo real.</span><span class="sxs-lookup"><span data-stu-id="af43c-133">Using script with VML enables you to create elements "on the fly" and manipulate attributes in real time.</span></span>

<span data-ttu-id="af43c-134">Esses exemplos nesta referência usam VBScript e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="af43c-134">This examples in this reference uses VBScript and Javascript.</span></span> <span data-ttu-id="af43c-135">Se usar uma linguagem de script diferente daquela mostrada em um exemplo, você deverá corresponder ao caso de todos os nomes de elementos e atributos.</span><span class="sxs-lookup"><span data-stu-id="af43c-135">If you use use a different scripting language than the one shown in an example, you must match the case of all element and attribute names.</span></span> <span data-ttu-id="af43c-136">A referência fornece a sintaxe de script correta para linguagens que diferenciam maiúsculas de minúsculas, como JavaScript.</span><span class="sxs-lookup"><span data-stu-id="af43c-136">The reference gives scripting syntax that is correct for case-sensitive languages such as JavaScript.</span></span> <span data-ttu-id="af43c-137">Se estiver em dúvida sobre o caso de caractere correto, use um pesquisador de objetos (como OLEView) para explorar o VGX.DLL para determinar o caso exato de um elemento ou atributo.</span><span class="sxs-lookup"><span data-stu-id="af43c-137">If in doubt regarding the correct character case, use an object browser (such as OLEView) to explore the VGX.DLL to determine the exact case of an element or attribute.</span></span> <span data-ttu-id="af43c-138">Observe que quando a VML é usada como marcações XML, a diferenciação de maiúsculas e minúsculas depende do tipo de documento do documento subjacente.</span><span class="sxs-lookup"><span data-stu-id="af43c-138">Note that when VML is used as XML tags, case sensitivity depends on the document type of you underlying document.</span></span> <span data-ttu-id="af43c-139">Se você estiver usando um modo estrito! DOCTYPE, elementos e atributos serão sensíveis a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="af43c-139">If you are using a strict mode !DOCTYPE, elements and attributes will be case sensitive.</span></span>

[<span data-ttu-id="af43c-140">A referência da VML</span><span class="sxs-lookup"><span data-stu-id="af43c-140">The VML Reference</span></span>](shape-element--vml.md)

 

 