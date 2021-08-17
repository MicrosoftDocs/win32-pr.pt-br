---
description: Os aplicativos podem usar PDH para extrair contadores de desempenho de logs SQL, ou podem extrair contadores formatados ou brutos diretamente do banco de dados por meio SQL consultas.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: SQL Esquema de arquivo de log
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: a95026c478094d8e71a44c2c57e65c2fa7044b00e982ea43187244838beed2ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143809"
---
# <a name="sql-log-file-schema"></a>SQL Esquema de arquivo de log

> [!IMPORTANT]
> Suporte a PDH para bancos de dados ODBC SQL podem ser alterados ou não disponíveis no futuro.

Os aplicativos podem usar apIs PDH para ler e gravar dados do contador de desempenho em bancos de dados compatíveis com SQL ODBC e, em seguida, executar processamento posterior por meio SQL consultas. Esta seção descreve o esquema SQL usado para armazenar contadores de desempenho. Você pode usar essas informações para criar exibições e relatórios personalizados. O esquema consiste nas três tabelas a seguir:

- [**Counterdata**](counterdata.md)
- [**CounterDetails**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> O suporte a PDH para bancos de dados SQL ODBC funciona apenas com drivers de SQL ODBC que dão suporte a extensões de cópia em [massa (BCP).](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions)
