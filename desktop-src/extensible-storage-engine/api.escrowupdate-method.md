---
description: 'Saiba mais sobre: método API. EscrowUpdate'
title: Método API. EscrowUpdate
TOCTitle: 'EscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.EscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.escrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100668
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dde632f01bd7ac9cbdf8bc4dc09e1337f32014b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646651"
---
# <a name="apiescrowupdate-method"></a><span data-ttu-id="d3617-103">Método API. EscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="d3617-103">Api.EscrowUpdate method</span></span>

<span data-ttu-id="d3617-104">Executar adição atômica em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="d3617-104">Perform atomic addition on one column.</span></span> <span data-ttu-id="d3617-105">A coluna deve ser do tipo [Long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="d3617-105">The column must be of type [Long](./jet-coltyp-enumeration.md).</span></span> <span data-ttu-id="d3617-106">Essa função permite que várias sessões atualizem o mesmo registro simultaneamente sem conflitos.</span><span class="sxs-lookup"><span data-stu-id="d3617-106">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

<span data-ttu-id="d3617-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d3617-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d3617-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d3617-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d3617-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3617-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function EscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Integer _
) As Integer
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Integer
Dim returnValue As Integer

returnValue = Api.EscrowUpdate(sesid, _
    tableid, columnid, delta)
```

``` csharp
public static int EscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int delta
)
```

#### <a name="parameters"></a><span data-ttu-id="d3617-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3617-110">Parameters</span></span>

  - <span data-ttu-id="d3617-111">sesid</span><span class="sxs-lookup"><span data-stu-id="d3617-111">sesid</span></span>  
    <span data-ttu-id="d3617-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3617-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d3617-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="d3617-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3617-114">TableID</span><span class="sxs-lookup"><span data-stu-id="d3617-114">tableid</span></span>  
    <span data-ttu-id="d3617-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3617-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d3617-116">O cursor a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="d3617-116">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3617-117">columnid</span><span class="sxs-lookup"><span data-stu-id="d3617-117">columnid</span></span>  
    <span data-ttu-id="d3617-118">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3617-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="d3617-119">A coluna a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="d3617-119">The column to update.</span></span> <span data-ttu-id="d3617-120">Deve ser uma coluna que pode ser atualizada com caução.</span><span class="sxs-lookup"><span data-stu-id="d3617-120">This must be an escrow-updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3617-121">delta</span><span class="sxs-lookup"><span data-stu-id="d3617-121">delta</span></span>  
    <span data-ttu-id="d3617-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d3617-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d3617-123">O Delta a ser aplicado à coluna.</span><span class="sxs-lookup"><span data-stu-id="d3617-123">The delta to apply to the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d3617-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3617-124">Return value</span></span>

<span data-ttu-id="d3617-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d3617-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="d3617-126">O valor atual da coluna como armazenado no banco de dados (o controle de versão é ignorado).</span><span class="sxs-lookup"><span data-stu-id="d3617-126">The current value of the column as stored in the database (versioning is ignored).</span></span>  

## <a name="remarks"></a><span data-ttu-id="d3617-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3617-127">Remarks</span></span>

<span data-ttu-id="d3617-128">Esse método encapsula [JetEscrowUpdate (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] Int32, \[ \] Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="d3617-128">This method wraps [JetEscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, \[\], Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d3617-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3617-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d3617-130">Referência</span><span class="sxs-lookup"><span data-stu-id="d3617-130">Reference</span></span>

[<span data-ttu-id="d3617-131">Classe de API</span><span class="sxs-lookup"><span data-stu-id="d3617-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d3617-132">Membros da API</span><span class="sxs-lookup"><span data-stu-id="d3617-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d3617-133">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d3617-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
