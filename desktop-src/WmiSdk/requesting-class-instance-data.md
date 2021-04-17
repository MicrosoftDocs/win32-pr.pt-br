---
description: 'As consultas de dados são instruções WQL que solicitam instâncias de classes. Para emitir uma consulta de dados, os aplicativos chamam o método IWbemServices:: ExecQuery ou IWbemServices:: ExecQueryAsync.'
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Solicitando dados de instância de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32df053ae1267f396978d98271f57f174ea6bf0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785000"
---
# <a name="requesting-class-instance-data"></a><span data-ttu-id="ea9ee-104">Solicitando dados de instância de classe</span><span class="sxs-lookup"><span data-stu-id="ea9ee-104">Requesting Class Instance Data</span></span>

<span data-ttu-id="ea9ee-105">As consultas de dados são instruções WQL que solicitam instâncias de classes.</span><span class="sxs-lookup"><span data-stu-id="ea9ee-105">Data queries are WQL statements that request instances of classes.</span></span> <span data-ttu-id="ea9ee-106">Para emitir uma consulta de dados, os aplicativos chamam o método [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) ou [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="ea9ee-106">To issue a data query, applications call the [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) or [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method.</span></span>

<span data-ttu-id="ea9ee-107">As instruções a seguir são usadas para fazer consultas de dados:</span><span class="sxs-lookup"><span data-stu-id="ea9ee-107">The following statements are used to make data queries:</span></span>

-   [<span data-ttu-id="ea9ee-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="ea9ee-108">SELECT</span></span>](select-statement-for-data-queries.md)
-   [<span data-ttu-id="ea9ee-109">ASSOCIADORES DE</span><span class="sxs-lookup"><span data-stu-id="ea9ee-109">ASSOCIATORS OF</span></span>](associators-of-statement.md)
-   [<span data-ttu-id="ea9ee-110">REFERÊNCIAS DE</span><span class="sxs-lookup"><span data-stu-id="ea9ee-110">REFERENCES OF</span></span>](references-of-statement.md)
-   [<span data-ttu-id="ea9ee-111">ISA</span><span class="sxs-lookup"><span data-stu-id="ea9ee-111">ISA</span></span>](isa-operator-for-data-queries.md)

<span data-ttu-id="ea9ee-112">A instrução WQL SELECT é a instrução de linguagem SQL padrão (SQL) para recuperar informações, com algumas restrições e extensões específicas do WQL.</span><span class="sxs-lookup"><span data-stu-id="ea9ee-112">The WQL SELECT statement is the standard Structured Query Language (SQL) statement for retrieving information, with a few restrictions and extensions specific to WQL.</span></span> <span data-ttu-id="ea9ee-113">Embora a instrução SQL SELECT seja normalmente usada no ambiente de banco de dados para recuperar colunas específicas de tabelas, a instrução WQL SELECT é usada no WMI para recuperar instâncias de uma única classe.</span><span class="sxs-lookup"><span data-stu-id="ea9ee-113">Although the SQL SELECT statement is typically used in the database environment to retrieve particular columns from tables, the WQL SELECT statement is used in WMI to retrieve instances of a single class.</span></span> <span data-ttu-id="ea9ee-114">O WQL não oferece suporte a consultas em várias classes.</span><span class="sxs-lookup"><span data-stu-id="ea9ee-114">WQL does not support queries across multiple classes.</span></span>

<span data-ttu-id="ea9ee-115">Os ASSOCIAdores de e referências de instruções são específicos do WQL e não fazem parte do SQL padrão.</span><span class="sxs-lookup"><span data-stu-id="ea9ee-115">The ASSOCIATORS OF and REFERENCES OF statements are specific to WQL and are not part of standard SQL.</span></span> <span data-ttu-id="ea9ee-116">A instrução ASSOCIATORS OF recupera todas as instâncias de classe associadas a uma instância de classe de origem específica e referências de recupera todas as instâncias que se referem a uma instância de origem específica.</span><span class="sxs-lookup"><span data-stu-id="ea9ee-116">The ASSOCIATORS OF statement retrieves all class instances that are associated with a particular source class instance, and REFERENCES OF retrieves all instances that refer to a particular source instance.</span></span> <span data-ttu-id="ea9ee-117">As associações são representadas por instâncias de uma [classe de associação](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="ea9ee-117">Associations are represented by instances of an [association class](declaring-an-association-class.md).</span></span>

 

 



