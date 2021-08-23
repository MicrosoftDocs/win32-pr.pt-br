---
title: Apêndice (VML)
description: Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Workshop da Web, namespaces
- Workshop da Web, estilos de comportamento
- projetando páginas da Web, namespaces
- projetando páginas da Web, estilos de comportamento
- linguagem VML (VML), namespaces
- VML (linguagem VML), namespaces
- gráficos vetoriais, namespaces
- linguagem VML (VML), estilos de comportamento
- Estilos de comportamento linguagem VML (VML)
- gráficos vetoriais, estilos de comportamento
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640de79138adcc345d4352ead814195007b88e0714a0f89816819d545e6e1ef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512606"
---
# <a name="appendix-vml"></a>Apêndice (VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Para permitir que os navegadores saibam como entregar dados para um processador específico do VML, você precisa digitar algumas informações, como namespaces e estilos de comportamento. Em seguida, você pode usar o VML para digitar gráficos na `<BODY>` região.

Neste tópico:

-   [Namespaces](#namespaces)
-   [Estilos de comportamento](#behavior-styles)

## <a name="namespaces"></a>Namespaces

Um mecanismo XML indica o namespace de onde um elemento vem. Se você alternar de análise em HTML para análise em XML, esse mecanismo indicará a opção em HTML.

Pergunte ao vendedor do processador VML quais informações são necessárias para o namespace XML.

Se você usar o Microsoft Internet Explorer para renderizar o VML, sempre digite a seguinte linha na `<HTML>` marca :


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



Essas informações informam Internet Explorer alternar para o namespace "urn:schemas-microsoft-com:vml" ao analisar uma marca XML com um prefixo e para entregar os dados resultantes para o processador `v:` VML.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="behavior-styles"></a>Estilos de comportamento

O VML é definido no Microsoft Internet Explorer como um comportamento padrão.

Para renderizar o VML, sempre digite as seguintes linhas na `<HEAD>` região:


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



O VML é implementado em Internet Explorer por meio VGX.DLL. Se a instalação inicial do navegador não incluir o comportamento do VML, talvez seja necessário adicioná-lo como uma opção. Você não precisa adicionar uma `<object>` marca.

 

 
