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
# <a name="using-the-textbox-element"></a>Usando o elemento TextBox

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

## <a name="examples"></a>Exemplos:

Para anexar texto a um retângulo, você pode digitar as seguintes linhas na `<BODY>` região da sua página da Web:


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





Para anexar um hiperlink a um retângulo arredondado que é preenchido com gradiente, você pode digitar as seguintes linhas na `<BODY>` região da sua página da Web:

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





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858397) .

 

 