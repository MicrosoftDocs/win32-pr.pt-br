---
title: Usando o elemento TextBox
description: Usando o elemento TextBox
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Web Workshop, elemento TextBox
- Criando páginas da Web, elemento TextBox
- Linguagem VML (VML), elemento TextBox
- VML (linguagem VML), elemento TextBox
- gráfico vetorial, elemento TextBox
- elemento TextBox
- Elementos da VML, caixa de texto
- Formas de VML, elemento TextBox
- Linguagem VML (VML), anexando texto
- VML (linguagem VML), anexando texto
- gráficos vetoriais, anexando texto
- Formas de VML, anexando texto
- anexando texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454316"
---
# <a name="using-the-textbox-element"></a><span data-ttu-id="4f965-116">Usando o elemento TextBox</span><span class="sxs-lookup"><span data-stu-id="4f965-116">Using the Textbox Element</span></span>

<span data-ttu-id="4f965-117">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4f965-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4f965-118">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="4f965-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4f965-119">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="4f965-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4f965-120">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="4f965-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4f965-121">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4f965-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4f965-122">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4f965-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="examples"></a><span data-ttu-id="4f965-123">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="4f965-123">Examples:</span></span>

<span data-ttu-id="4f965-124">Para anexar texto a um retângulo, você pode digitar as seguintes linhas na `<BODY>` região da sua página da Web:</span><span class="sxs-lookup"><span data-stu-id="4f965-124">To attach text to a rectangle, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





<span data-ttu-id="4f965-125">Para anexar um hiperlink a um retângulo arredondado que é preenchido com gradiente, você pode digitar as seguintes linhas na `<BODY>` região da sua página da Web:</span><span class="sxs-lookup"><span data-stu-id="4f965-125">To attach a hyperlink to a rounded rectangle that is gradient-filled, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![textbox2.gif (1147 bytes)](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





<span data-ttu-id="4f965-127">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span><span class="sxs-lookup"><span data-stu-id="4f965-127">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span></span>

 

 