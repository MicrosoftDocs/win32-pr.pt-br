---
description: Para selecionar uma NIC de uma tabela de BLOB NPP retornada por Monitor de Rede, chame a função GetNPPBlobTable. Essa função retorna uma tabela de BLOB NPP, que pode ser enumerada por seu aplicativo para selecionar a NIC na qual você está interessado.
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: Selecionando uma NIC de uma tabela de BLOB NPP retornada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08215bb647482ba8544d7eaa033dea7efd9a5ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828422"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a><span data-ttu-id="52712-104">Selecionando uma NIC de uma tabela de BLOB NPP retornada</span><span class="sxs-lookup"><span data-stu-id="52712-104">Selecting a NIC from a Returned NPP BLOB table</span></span>

<span data-ttu-id="52712-105">Para selecionar uma NIC de uma tabela de BLOB NPP retornada por Monitor de Rede, chame a função [**GetNPPBlobTable**](getnppblobtable.md) .</span><span class="sxs-lookup"><span data-stu-id="52712-105">To select a NIC from an NPP BLOB table returned by Network Monitor, call the [**GetNPPBlobTable**](getnppblobtable.md) function.</span></span> <span data-ttu-id="52712-106">Essa função retorna uma tabela de BLOB NPP, que pode ser enumerada por seu aplicativo para selecionar a NIC na qual você está interessado.</span><span class="sxs-lookup"><span data-stu-id="52712-106">This function returns an NPP BLOB table, which can then be enumerated by your application to select the NIC you are interested in.</span></span>

<span data-ttu-id="52712-107">Ao chamar essa função, você pode retornar uma tabela de BLOB de todas as NICs registradas no computador local ou em um conjunto menor de NICs filtradas.</span><span class="sxs-lookup"><span data-stu-id="52712-107">When you call this function you can return either a BLOB table of all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="52712-108">Para filtrar as NICs que são retornadas, você pode fornecer um [*blob de filtro*](f.md) quando a chamada é feita.</span><span class="sxs-lookup"><span data-stu-id="52712-108">To filter the NICs that are returned, you can provide a [*filter BLOB*](f.md) when the call is made.</span></span>



| <span data-ttu-id="52712-109">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="52712-109">For information about</span></span>                                                       | <span data-ttu-id="52712-110">Consulte</span><span class="sxs-lookup"><span data-stu-id="52712-110">See</span></span>                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52712-111">Como especificar um filtro que limita as NICs retornadas em uma tabela de BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="52712-111">How to specify a filter that limits the NICs returned in an NPP BLOB table.</span></span> | [<span data-ttu-id="52712-112">Especificando um BLOB de filtro</span><span class="sxs-lookup"><span data-stu-id="52712-112">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="52712-113">Como selecionar uma NIC registrada em um computador local.</span><span class="sxs-lookup"><span data-stu-id="52712-113">How to select a NIC registered on a local computer.</span></span>                         | [<span data-ttu-id="52712-114">Selecionando uma NIC registrada</span><span class="sxs-lookup"><span data-stu-id="52712-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="52712-115">Como selecionar uma NIC de uma tabela de BLOB NPP fornecida</span><span class="sxs-lookup"><span data-stu-id="52712-115">How to select a NIC from a supplied NPP BLOB table</span></span>                          | [<span data-ttu-id="52712-116">Selecionando uma NIC de uma tabela de BLOB NPP fornecida</span><span class="sxs-lookup"><span data-stu-id="52712-116">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



