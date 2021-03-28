---
description: Os identificadores InputLocale e keywordlocale ajudam o mecanismo de pesquisa a usar os separadores de palavras corretos identificando o idioma das consultas inseridas pelo usuário e o idioma do das palavras-chave da sintaxe de consulta avançada.
title: Argumentos de identificador de localidade (o Shell do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 403e0338b61a4dedba37a620000e3fd82c91f383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171549"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a>Argumentos de identificador de localidade (o Shell do Windows)

Os `inputlocale` `keywordlocale` identificadores e ajudam o mecanismo de pesquisa a usar os separadores de palavras corretos identificando o idioma das consultas inseridas pelo usuário e o idioma o das palavras-chave da sintaxe de consulta avançada. Esses nem sempre são os mesmos identificadores de código de linguagem (LCIDs) porque o Windows Search é oferecido em várias versões internacionais e também inclui pacotes MUI (Multilingual User interface) para mais idiomas. O `inputlocale` identifica o LCID para os usuários de idioma que inserim sua consulta de pesquisa no, enquanto o `keywordlocale` identifica o LCID que o mecanismo de pesquisa usa para palavras-chave.

## <a name="example"></a>Exemplo


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a>Informações do argumento



|                          |                                         |
|--------------------------|-----------------------------------------|
| Sistema operacional mínimo | Windows Vista com Service Pack 1 (SP1) |



 

 

 



