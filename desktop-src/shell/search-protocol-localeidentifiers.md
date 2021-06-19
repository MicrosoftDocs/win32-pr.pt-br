---
description: Entenda os argumentos inputlocale e keywordlocale na interface do usuário do Windows Shell, o que ajuda o mecanismo de pesquisa a usar os disjuntores de palavras corretos.
title: Argumentos de identificador de localidade (o Shell do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 34eab39e7ed956bf68048d9ce5861c12eedbbe7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403589"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a>Argumentos de identificador de localidade (o Shell do Windows)

Os identificadores e ajudam o mecanismo de pesquisa a usar os disjuntores de palavras corretos identificando o idioma das consultas inseridas pelo usuário e o idioma das palavras-chave de Sintaxe de Consulta `inputlocale` `keywordlocale` Avançada. Nem sempre são os mesmos LCIDs (identificadores de código de idioma), pois o Windows Search é oferecido em várias versões internacionais e também inclui pacotes Interface de Usuário Multilíngue (MUI) para mais idiomas. O identifica o LCID para a linguagem em que os usuários insejam sua consulta de pesquisa, enquanto o identifica o LCID que o mecanismo de pesquisa usa para `inputlocale` `keywordlocale` palavras-chave.

## <a name="example"></a>Exemplo


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a>Informações de argumento



|                              | Valor                                   |
|------------------------------|-----------------------------------------|
| **Sistema operacional mínimo** | Windows Vista com Service Pack 1 (SP1) |



 

 

 



