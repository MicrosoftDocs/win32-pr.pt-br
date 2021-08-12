---
title: Atributo TableProperties do VML
description: Atributo TableProperties do VML
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050e290bc4b779fec40ebf3ad3fb202b34af23b10f70a0070038c56f5f8ea2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597542"
---
# <a name="vml-tableproperties-attribute"></a>Atributo TableProperties do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina as propriedades da tabela. Leitura/gravação. **Integer**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* o:tableproperties=" *expressão* ">

**Comentários**

Usado pelo Microsoft PowerPoint para tabelas nativas. O valor padrão é 0. Somente os três primeiros bits desse inteiro são usados.

Embora o valor seja armazenado em uma forma, o atributo só é útil quando a tabela é feita de formas agrupadas. Os bits podem ser combinados.

Os valores de bit a seguir são incluídos.



| bit | Descrição                              |
|-----|------------------------------------------|
| 1   | Definir se o grupo de formas for uma tabela.   |
| 2   | Definir se a forma for um espaço reservado.       |
| 3   | Definir se o texto da tabela for bi-direcional. |



 

*Microsoft Office Atributo Extensions*

 

 