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
# <a name="sql-log-file-schema"></a><span data-ttu-id="d5490-103">Esquema do arquivo de log SQL</span><span class="sxs-lookup"><span data-stu-id="d5490-103">SQL Log File Schema</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5490-104">O suporte da PDH para bancos de dados ODBC SQL pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="d5490-104">PDH support for ODBC SQL databases may be altered or unavailable in the future.</span></span>

<span data-ttu-id="d5490-105">Os aplicativos podem usar as APIs de PDH de leitura e gravação de dados do contador de desempenho em bancos de dado SQL ODBC compatíveis e, em seguida, executar processamento adicional por meio de consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="d5490-105">Applications can use PDH APIs read and write performance counter data in compatible ODBC SQL databases and then perform further processing through SQL queries.</span></span> <span data-ttu-id="d5490-106">Esta seção descreve o esquema SQL usado para armazenar contadores de desempenho.</span><span class="sxs-lookup"><span data-stu-id="d5490-106">This section describes the SQL schema used to store performance counters.</span></span> <span data-ttu-id="d5490-107">Você pode usar essas informações para criar relatórios e exibições personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d5490-107">You can use this information to create custom views and reports.</span></span> <span data-ttu-id="d5490-108">O esquema consiste nas três tabelas a seguir:</span><span class="sxs-lookup"><span data-stu-id="d5490-108">The schema consists of the following three tables:</span></span>

- [<span data-ttu-id="d5490-109">**Dados**</span><span class="sxs-lookup"><span data-stu-id="d5490-109">**CounterData**</span></span>](counterdata.md)
- [<span data-ttu-id="d5490-110">**Detalhes**</span><span class="sxs-lookup"><span data-stu-id="d5490-110">**CounterDetails**</span></span>](counterdetails.md)
- [<span data-ttu-id="d5490-111">**DisplayToID**</span><span class="sxs-lookup"><span data-stu-id="d5490-111">**DisplayToID**</span></span>](displaytoid.md)

> [!NOTE]
> <span data-ttu-id="d5490-112">O suporte da PDH para bancos de dados ODBC SQL funciona apenas com drivers ODBC SQL que dão suporte a [extensões de cópia em massa (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span><span class="sxs-lookup"><span data-stu-id="d5490-112">PDH support for ODBC SQL databases only works with ODBC SQL drivers that support [Bulk Copy (BCP) Extensions](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span></span>
