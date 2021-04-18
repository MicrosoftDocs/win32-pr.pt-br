---
title: Atributo de impressão de VML
description: Atributo de impressão de VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810276"
---
# <a name="vml-print-attribute"></a>Atributo de impressão de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se a forma será impressa. Leitura/gravação. [VgTriState](msdn-online-vml-vgtristate.md).

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* Print = " *expressão* " >

**Sintaxe do script**

*elemento* . Print = "*expressão*"

*expressão* = de *elemento*. Print

**Comentários**

Fornecido como uma maneira de especificar se as formas serão impressas. Observe que uma forma ainda pode ser exibida na tela, mesmo que não seja impressa como resultado desse atributo ser **falso**. O valor padrão é **True**.

Esse atributo é usado pelo Microsoft Office, mas não é usado pelo Microsoft Internet Explorer.

*Atributo de extensões de Microsoft Office*

 

 