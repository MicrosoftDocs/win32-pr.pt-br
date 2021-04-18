---
description: A linguagem de consulta do Microsoft Windows Search baseia-se em linguagem SQL (SQL); no entanto, ele não pesquisa em um banco de dados relacional com tabelas ou índices definidos pelo usuário.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: Recursos do SQL não disponíveis no Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793629"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>Recursos do SQL não disponíveis no Microsoft Windows Search

A linguagem de consulta do Microsoft Windows Search baseia-se em linguagem SQL (SQL); no entanto, ele não pesquisa em um banco de dados relacional com tabelas ou índices definidos pelo usuário. Por isso, muitas instruções SQL padrão e recursos de sintaxe não se aplicam. A seguir está uma lista dos recursos SQL mais significativos que não têm suporte no Windows Search.


-   Instruções de lote
-   Função de \_ tabela de adesão
-   Função CONVERT (use as funções CAST em vez disso)
-   instrução CREATE VIEW
-   Linguagem de definição de dados
-   Instrução DATASOURCE
-   Formatos de data e hora diferentes de data e hora ISO
-   Instrução DELETE
-   instrução GRANT
-   Esquema de informações
-   Instrução INSERT
-   Tipos de dados OLE DB
-   SQL-expressões regulares padrão (use CONTAINS ou LIKE em vez disso)
-   Parâmetros para consultas SQL
-   Comparação de coluna relacional
-   Cabeçalho da ID de revisão
-   instrução REVOKE
-   Aliases de escopo ou números de revisão
-   SELECIONAR tudo (remove duplicatas automaticamente)
-   Procedimentos armazenados
-   Expansão de documento estruturado
-   TODOS UNION
-   Palavra-chave desconhecida
-   Instrução UPDATE

O Windows Search não dá suporte a palavras de dicionário de sinônimos e de ruído.

 

 



