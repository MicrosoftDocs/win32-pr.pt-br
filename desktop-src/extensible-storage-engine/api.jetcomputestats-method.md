---
description: 'Saiba mais sobre: método API. JetComputeStats'
title: Método API. JetComputeStats
TOCTitle: 'JetComputeStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetComputeStats(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcomputestats(v=EXCHG.10)
ms:contentKeyID: 55100667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b102aca5971656232fae02684aeab30322d208b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164237"
---
# <a name="apijetcomputestats-method"></a><span data-ttu-id="8cc33-103">Método API. JetComputeStats</span><span class="sxs-lookup"><span data-stu-id="8cc33-103">Api.JetComputeStats method</span></span>

<span data-ttu-id="8cc33-104">Percorre cada índice de uma tabela para calcular exatamente o número de entradas em um índice e o número de chaves distintas em um índice.</span><span class="sxs-lookup"><span data-stu-id="8cc33-104">Walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="8cc33-105">Essas informações, junto com o número de páginas de banco de dados alocadas para um índice e a hora atual da computação, são armazenadas em metadados de índice no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8cc33-105">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="8cc33-106">Esses dados podem ser recuperados posteriormente com operações de informações.</span><span class="sxs-lookup"><span data-stu-id="8cc33-106">This data can be subsequently retrieved with information operations.</span></span>

<span data-ttu-id="8cc33-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8cc33-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8cc33-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8cc33-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc33-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cc33-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetComputeStats ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetComputeStats(sesid, tableid)
```

``` csharp
public static void JetComputeStats(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="8cc33-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cc33-110">Parameters</span></span>

  - <span data-ttu-id="8cc33-111">sesid</span><span class="sxs-lookup"><span data-stu-id="8cc33-111">sesid</span></span>  
    <span data-ttu-id="8cc33-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8cc33-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8cc33-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="8cc33-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8cc33-114">TableID</span><span class="sxs-lookup"><span data-stu-id="8cc33-114">tableid</span></span>  
    <span data-ttu-id="8cc33-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8cc33-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8cc33-116">A tabela na qual as estatísticas serão computadas.</span><span class="sxs-lookup"><span data-stu-id="8cc33-116">The table that the statistics will be computed on.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cc33-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cc33-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8cc33-118">Referência</span><span class="sxs-lookup"><span data-stu-id="8cc33-118">Reference</span></span>

[<span data-ttu-id="8cc33-119">Classe de API</span><span class="sxs-lookup"><span data-stu-id="8cc33-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8cc33-120">Membros da API</span><span class="sxs-lookup"><span data-stu-id="8cc33-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8cc33-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8cc33-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
