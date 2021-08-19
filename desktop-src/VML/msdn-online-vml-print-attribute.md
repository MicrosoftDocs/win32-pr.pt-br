---
title: Atributo de impressão VML
description: Atributo de impressão VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfa364e573d887da2013f946ddf23e0a974e0f63211623de3d2046b0525b2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057724"
---
# <a name="vml-print-attribute"></a>Atributo de impressão VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se a forma será impressa. Leitura/gravação. [VgTriState.](msdn-online-vml-vgtristate.md)

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* print=" *expressão* ">

**Sintaxe do script**

*expressão element* .print=""

*expressão* = *elemento*.print

**Comentários**

Fornecido como uma maneira de especificar se as formas serão impressas. Observe que uma forma ainda pode ser exibida na tela, mesmo que ela não seja impressa como resultado desse atributo ser **False.** O valor padrão é **True**.

Esse atributo é usado pelo Microsoft Office, mas não é usado pelo Microsoft Internet Explorer.

*Microsoft Office Atributo Extensions*

 

 