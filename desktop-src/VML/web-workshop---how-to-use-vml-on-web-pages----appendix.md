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
# <a name="appendix-vml"></a>Apêndice (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Para permitir que os navegadores saibam como entregar os dados a um processador específico da VML, você precisa digitar algumas informações, como namespaces e estilos de comportamento. Em seguida, você pode usar a VML para digitar elementos gráficos na `<BODY>` região.

Neste tópico:

-   [Namespaces](#namespaces)
-   [Estilos de comportamento](#behavior-styles)

## <a name="namespaces"></a>Namespaces

Um mecanismo XML indica o namespace do qual um elemento é proveniente. Se você alternar da análise em HTML para analisar em XML, esse mecanismo indicará o comutador em HTML.

Pergunte ao fornecedor do seu processador VML quais informações são necessárias para o namespace XML.

Se você usar o Microsoft Internet Explorer para renderizar a VML, sempre digite a seguinte linha na `<HTML>` marca:


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



Essas informações dizem ao Internet Explorer para mudar para o namespace "urn: schemas-microsoft-com: VML" ao analisar uma marca XML com um prefixo `v:` e para entregar os dados resultantes para o processador da VML.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="behavior-styles"></a>Estilos de comportamento

A VML é definida no Microsoft Internet Explorer como um comportamento padrão.

Para renderizar a VML, sempre digite as seguintes linhas na `<HEAD>` região:


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



A VML é implementada no Internet Explorer por meio de VGX.DLL. Se a instalação inicial do navegador não incluía o comportamento de VML, talvez seja necessário adicioná-lo como uma opção. Você não precisa adicionar uma `<object>` marca.

 

 
