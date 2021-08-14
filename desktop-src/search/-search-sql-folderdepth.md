---
description: Predicados de profundidade de pasta controlam o escopo de uma pesquisa especificando um caminho e se devem ser executadas uma passagem profunda ou superficial.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Predicados de escopo e diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f221ba4048f1ab7f5096321cc00aed209acb5ca3e5616e6e6a4fbbc516dfc28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462465"
---
# <a name="scope-and-directory-predicates"></a>Predicados de escopo e diretório

Predicados de profundidade de pasta controlam o escopo de uma pesquisa especificando um caminho e se devem ser executadas uma passagem profunda ou superficial. O seguinte mostra a sintaxe dos predicados de profundidade de pasta:


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



O predicado é seguido por um sinal de igual. O caminho é revelado entre aspas simples e deve começar com um protocolo e dois-pontos (por exemplo,, `file:` `mapi:` ou `csc:` ). O predicado de escopo executa uma passagem profunda do caminho, incluindo todas as subpastas, enquanto o predicado de diretório faz uma passagem superficial apenas da pasta especificada. assim como outras restrições de linguagem SQL (SQL), você pode especificar mais de uma restrição de profundidade de pasta em uma única consulta.

Para consultar o catálogo local de um computador remoto, inclua o nome do computador antes do catálogo e um caminho UNC (Convenção de nomenclatura universal) no computador remoto na cláusula SCOPE ou DIRECTORY.

## <a name="examples"></a>Exemplos


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



O primeiro exemplo de escopo pesquisa a pasta C: \\ files \\ reports e todas as suas subpastas. O exemplo de diretório pesquisa apenas a pasta raiz C: \\ files \\ reports.

> [!Note]  
> As barras invertidas do sistema de arquivos ( \\ ) tornam-se marcas de barras de estilo de URL (às vezes chamadas de barras "/)".

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Cláusula FROM](-search-sql-from.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> </dl>

 

 



