---
description: Os aplicativos podem usar a PDH para extrair contadores de desempenho de logs SQL ou podem extrair contadores formatados ou brutos diretamente do banco de dados por meio de consultas SQL.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: Esquema do arquivo de log SQL
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756876"
---
# <a name="sql-log-file-schema"></a>Esquema do arquivo de log SQL

> [!IMPORTANT]
> O suporte da PDH para bancos de dados ODBC SQL pode ser alterado ou indisponível no futuro.

Os aplicativos podem usar as APIs de PDH de leitura e gravação de dados do contador de desempenho em bancos de dado SQL ODBC compatíveis e, em seguida, executar processamento adicional por meio de consultas SQL. Esta seção descreve o esquema SQL usado para armazenar contadores de desempenho. Você pode usar essas informações para criar relatórios e exibições personalizadas. O esquema consiste nas três tabelas a seguir:

- [**Dados**](counterdata.md)
- [**Detalhes**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> O suporte da PDH para bancos de dados ODBC SQL funciona apenas com drivers ODBC SQL que dão suporte a [extensões de cópia em massa (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).
