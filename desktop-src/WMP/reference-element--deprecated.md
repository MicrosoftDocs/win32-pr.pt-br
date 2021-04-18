---
title: Elemento Reference (preterido)
description: Elemento Reference (preterido)
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Metaarquivos do Windows Media, elemento Reference
- Metafiles, elemento Reference
- elemento Reference
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105784691"
---
# <a name="reference-element-deprecated"></a>Elemento Reference (preterido)

Este tópico documenta um recurso que não é mais usado na versão atual dos metaarquivos do Windows Media.

O elemento **Reference** contém uma lista de referências a URLs. Cada item na lista tem o formato Ref *XX*  =  *URL*, em que *XX* é um inteiro e a *URL* é a URL de um arquivo ASF (Advanced Systems Format).

**Sintaxe**


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



Os inteiros representados por *XX* devem estar em ordem crescente. Ou seja, o número inteiro em cada linha deve ser maior que o inteiro na linha anterior.

Quando um programa cliente lê um elemento de referência, ele tenta se conectar ao arquivo de mídia representado pela primeira URL na lista. Se isso falhar, o programa cliente tentará se conectar ao arquivo representado pela próxima URL na lista. O programa cliente continua a lista até que faça uma conexão bem-sucedida ou atinja o final da lista. Observe que, se o programa cliente fizer uma conexão bem-sucedida, ele não lerá nenhuma das URLs subsequentes na lista.

**Código de exemplo**

No exemplo a seguir, o programa cliente tentaria primeiro se conectar ao arquivo representado pela URL MMS. Se isso falhar, o programa cliente tentaria se conectar ao arquivo representado pela URL http.


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a>Comentários

O formato de arquivo ASF abrange uma ampla variedade de tipos de mídia, incluindo áudio e vídeo. Os arquivos ASF também usam várias extensões de nome de arquivo diferentes, incluindo. WMA e. wmv.

Os inteiros representados por *XX* devem estar em ordem crescente. Ou seja, o número inteiro em cada linha deve ser maior que o inteiro na linha anterior.

Quando um programa cliente lê um elemento de referência, ele tenta se conectar ao arquivo de mídia representado pela primeira URL na lista. Se isso falhar, o programa cliente tentará se conectar ao arquivo representado pela próxima URL na lista. O programa cliente continua a lista até que faça uma conexão bem-sucedida ou atinja o final da lista. Observe que, se o programa cliente fizer uma conexão bem-sucedida, ele não lerá nenhuma das URLs subsequentes na lista.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Versões anteriores de metaarquivos do Windows Media (preterido)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




