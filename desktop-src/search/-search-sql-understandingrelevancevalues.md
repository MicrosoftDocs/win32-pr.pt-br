---
description: Em um banco de dados relacional, as linhas retornadas por uma consulta de pesquisa devem atender a todas as condições chamadas para pela consulta. Por outro lado, uma consulta do Windows Search pode retornar documentos que atendam aos critérios de pesquisa a graus variados.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Noções básicas sobre valores de relevância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826905"
---
# <a name="understanding-relevance-values"></a>Noções básicas sobre valores de relevância

Em um banco de dados relacional, as linhas retornadas por uma consulta de pesquisa devem atender a todas as condições chamadas para pela consulta. Por outro lado, uma consulta do Windows Search pode retornar documentos que atendam aos critérios de pesquisa a graus variados.

Por exemplo, uma pesquisa pelo termo "programa" em um banco de dados relacional produz registros que contêm essa grafia específica da palavra. Se um registro contém uma ou 100 instâncias da palavra não tem impacto sobre os resultados. Por outro lado, o Windows Search retorna um valor de relevância associado aos documentos correspondentes. A relevância dos documentos com "programa" no título é maior que aqueles que contêm a palavra somente no último parágrafo. Da mesma forma, os documentos que contêm variações do termo de pesquisa, por exemplo, "programas" e "programação" também correspondem e são retornados pela consulta.

As consultas do Windows Search retornam valores de relevância de inteiros na coluna chamada "Rank".

Além disso:

-   Os valores de classificação retornados pela consulta são inteiros variando de 0 a 1000.
-   Valores de classificação mais altos indicam documentos que correspondem melhor às condições de pesquisa.
-   Os valores de classificação se aplicam somente à consulta atual, portanto, eles não podem ser comparados aos resultados entre consultas.
-   Os valores de classificação são relativos aos outros documentos que correspondem à consulta. Portanto, o valor de classificação de um documento específico depende dos outros documentos que também correspondem à consulta.
-   Valores de classificação para itens que correspondem a um predicado puramente relacional são 1000.

Você pode manipular os valores de classificação retornados usando pesos de coluna nos predicados de cláusula [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) Where e a cláusula Rank by.

 

 



