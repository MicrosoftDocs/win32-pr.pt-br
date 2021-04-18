---
title: Atributo de tabela da VML
description: Atributo de tabela da VML
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105784960"
---
# <a name="vml-tableproperties-attribute"></a>Atributo de tabela da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina as propriedades da tabela. Leitura/gravação. **Integer**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* o:TableProperties = " *expressão* " >

**Comentários**

Usado pelo Microsoft PowerPoint para tabelas nativas. O valor padrão é 0. Somente os três primeiros bits deste inteiro são usados.

Embora o valor seja armazenado em uma forma, o atributo só é útil quando a tabela é composta de formas agrupadas. Os bits podem ser combinados.

Os valores de bit a seguir estão incluídos.



| bit | Descrição                              |
|-----|------------------------------------------|
| 1   | Defina se o grupo de formas é uma tabela.   |
| 2   | Defina se a forma é um espaço reservado.       |
| 3   | Defina se o texto da tabela é bidirecional. |



 

*Atributo de extensões de Microsoft Office*

 

 