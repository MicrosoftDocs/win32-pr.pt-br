---
description: O predicado CONTAINS dá suporte ao uso do asterisco ( \* ) como um caractere curinga para representar palavras e frases. Você pode adicionar o asterisco somente no final da palavra ou frase. A presença do asterisco habilita o modo de correspondência de prefixo.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Usando caracteres curinga no predicado CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090059"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a>Usando caracteres curinga no predicado CONTAINS

O predicado CONTAINS dá suporte ao uso do asterisco ( \* ) como um caractere curinga para representar palavras e frases. Você pode adicionar o asterisco somente no final da palavra ou frase. A presença do asterisco habilita o modo de correspondência de prefixo. Nesse modo, as correspondências serão retornadas se a coluna contiver a palavra de pesquisa especificada seguida por zero ou mais caracteres. Se uma frase for fornecida, as correspondências serão detectadas se a coluna contiver todas as palavras especificadas com zero ou mais caracteres após a palavra final.

## <a name="examples"></a>Exemplos

O primeiro exemplo corresponde a documentos que têm qualquer palavra na coluna FileName que começa com "serv". Exemplos de palavras correspondentes incluem "servidor", "servidores" e "serviço".


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



O segundo exemplo corresponde a documentos com qualquer frase na coluna FileName que começa com "comp" e na qual a próxima palavra começa com "serv". Exemplos de palavras de correspondência incluem "servidor de comp", "servidores de comp" e "serviço de comp".


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



O asterisco só funciona para correspondência de prefixo e pode ser posicionado somente no final da palavra ou frase; Ele não funciona para correspondência de sufixo. A sintaxe a seguir não é válida e não corresponde a documentos com nenhuma palavra na coluna FileName que termina com "servi".


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Predicado FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> </dl>

 

 



