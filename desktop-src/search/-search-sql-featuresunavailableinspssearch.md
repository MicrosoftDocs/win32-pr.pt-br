---
description: A Windows de consulta do Microsoft Windows Search é baseada em linguagem SQL (SQL); no entanto, ele não pesquisa em um banco de dados relacional com tabelas ou índices definidos pelo usuário.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: SQL Recursos indisponíveis no Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66adb175aa7fae799e0ad9b69916415f12c94ee984d276b5a2238ebb19ec2f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716116"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>SQL Recursos indisponíveis no Microsoft Windows Search

A Windows de consulta do Microsoft Windows Search é baseada em linguagem SQL (SQL); no entanto, ele não pesquisa em um banco de dados relacional com tabelas ou índices definidos pelo usuário. Por isso, muitas instruções SQL padrão e recursos de sintaxe não se aplicam. Veja a seguir uma lista dos recursos de SQL mais significativos que não têm suporte no Windows Search.


-   Instruções BATCH
-   Função COALESCE \_ TABLE
-   Função CONVERT (use as funções CAST em vez disso)
-   instrução CREATE VIEW
-   Linguagem de definição de dados
-   Instrução DATASOURCE
-   Formatos de data e hora diferentes do carimbo de data e hora ISO
-   Instrução DELETE
-   instrução GRANT
-   Esquema de informações
-   Instrução INSERT
-   OLE DB de dados
-   SQL regulares padrão do SQL (use CONTAINS ou LIKE em vez disso)
-   Parâmetros para SQL consultas
-   Comparação de coluna relacional
-   Header de ID de revisão
-   instrução REVOKE
-   Aliases scope ou números de revisão
-   SELECT ALL (remove duplicatas automaticamente)
-   Procedimentos armazenados
-   Expansão de documentos estruturados
-   TODOS UNION
-   Palavra-chave UNKNOWN
-   Instrução UPDATE

Windows A pesquisa não dá suporte a Dicionário de Sinônimos e Palavras de Ruído.

 

 



