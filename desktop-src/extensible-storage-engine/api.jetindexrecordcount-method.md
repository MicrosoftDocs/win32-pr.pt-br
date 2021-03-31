---
description: 'Saiba mais sobre: método API. JetIndexRecordCount'
title: Método API. JetIndexRecordCount
TOCTitle: 'JetIndexRecordCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetindexrecordcount(v=EXCHG.10)
ms:contentKeyID: 55100758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 429239ab7734a594fd2c5a3510650d8f410e94f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663131"
---
# <a name="apijetindexrecordcount-method"></a><span data-ttu-id="776c7-103">Método API. JetIndexRecordCount</span><span class="sxs-lookup"><span data-stu-id="776c7-103">Api.JetIndexRecordCount method</span></span>

<span data-ttu-id="776c7-104">Conta o número de entradas no índice atual a partir da posição atual para frente.</span><span class="sxs-lookup"><span data-stu-id="776c7-104">Counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="776c7-105">A posição atual é incluída na contagem.</span><span class="sxs-lookup"><span data-stu-id="776c7-105">The current position is included in the count.</span></span> <span data-ttu-id="776c7-106">A contagem pode ser maior que o número total de registros na tabela se o índice atual estiver sobre uma coluna de valores múltiplos e as instâncias da coluna tiverem vários valores.</span><span class="sxs-lookup"><span data-stu-id="776c7-106">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="776c7-107">Se a tabela estiver vazia, 0 será retornado para a contagem.</span><span class="sxs-lookup"><span data-stu-id="776c7-107">If the table is empty, then 0 will be returned for the count.</span></span>

<span data-ttu-id="776c7-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="776c7-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="776c7-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="776c7-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="776c7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="776c7-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIndexRecordCount ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef numRecords As Integer, _
    maxRecordsToCount As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRecords As Integer
Dim maxRecordsToCount As IntegerApi.JetIndexRecordCount(sesid, _
    tableid, numRecords, maxRecordsToCount)
```

``` csharp
public static void JetIndexRecordCount(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int numRecords,
    int maxRecordsToCount
)
```

#### <a name="parameters"></a><span data-ttu-id="776c7-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="776c7-111">Parameters</span></span>

  - <span data-ttu-id="776c7-112">sesid</span><span class="sxs-lookup"><span data-stu-id="776c7-112">sesid</span></span>  
    <span data-ttu-id="776c7-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="776c7-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="776c7-114">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="776c7-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="776c7-115">TableID</span><span class="sxs-lookup"><span data-stu-id="776c7-115">tableid</span></span>  
    <span data-ttu-id="776c7-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="776c7-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="776c7-117">O cursor para contar os registros.</span><span class="sxs-lookup"><span data-stu-id="776c7-117">The cursor to count the records in.</span></span>

<!-- end list -->

  - <span data-ttu-id="776c7-118">numRecords</span><span class="sxs-lookup"><span data-stu-id="776c7-118">numRecords</span></span>  
    <span data-ttu-id="776c7-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="776c7-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="776c7-120">Retorna o número de registros.</span><span class="sxs-lookup"><span data-stu-id="776c7-120">Returns the number of records.</span></span>

<!-- end list -->

  - <span data-ttu-id="776c7-121">maxRecordsToCount</span><span class="sxs-lookup"><span data-stu-id="776c7-121">maxRecordsToCount</span></span>  
    <span data-ttu-id="776c7-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="776c7-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="776c7-123">O número máximo de registros a serem contados.</span><span class="sxs-lookup"><span data-stu-id="776c7-123">The maximum number of records to count.</span></span> <span data-ttu-id="776c7-124">Um valor de 0 indica que a contagem é ilimitada.</span><span class="sxs-lookup"><span data-stu-id="776c7-124">A value of 0 indicates that the count is unlimited.</span></span>

## <a name="see-also"></a><span data-ttu-id="776c7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="776c7-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="776c7-126">Referência</span><span class="sxs-lookup"><span data-stu-id="776c7-126">Reference</span></span>

[<span data-ttu-id="776c7-127">Classe de API</span><span class="sxs-lookup"><span data-stu-id="776c7-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="776c7-128">Membros da API</span><span class="sxs-lookup"><span data-stu-id="776c7-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="776c7-129">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="776c7-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
