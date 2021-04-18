---
description: 'Saiba mais sobre: método API. JetEscrowUpdate'
title: Método API. JetEscrowUpdate
TOCTitle: 'JetEscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetescrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100740
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 09e74f964fd6018248a3cfc594621bed96f92e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814585"
---
# <a name="apijetescrowupdate-method"></a><span data-ttu-id="9997b-103">Método API. JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="9997b-103">Api.JetEscrowUpdate method</span></span>

<span data-ttu-id="9997b-104">Executa uma operação de adição atômica em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="9997b-104">Performs an atomic addition operation on one column.</span></span> <span data-ttu-id="9997b-105">Essa função permite que várias sessões atualizem o mesmo registro simultaneamente sem conflitos.</span><span class="sxs-lookup"><span data-stu-id="9997b-105">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span> <span data-ttu-id="9997b-106">Consulte também [EscrowUpdate (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="9997b-106">Also see [EscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span></span>

<span data-ttu-id="9997b-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9997b-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9997b-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9997b-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9997b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9997b-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Byte(), _
    deltaSize As Integer, _
    previousValue As Byte(), _
    previousValueLength As Integer, _
    <OutAttribute> ByRef actualPreviousValueLength As Integer, _
    grbit As EscrowUpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Byte()
Dim deltaSize As Integer
Dim previousValue As Byte()
Dim previousValueLength As Integer
Dim actualPreviousValueLength As Integer
Dim grbit As EscrowUpdateGrbitApi.JetEscrowUpdate(sesid, tableid, _
    columnid, delta, deltaSize, previousValue, _
    previousValueLength, actualPreviousValueLength, _
    grbit)
```

``` csharp
public static void JetEscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] delta,
    int deltaSize,
    byte[] previousValue,
    int previousValueLength,
    out int actualPreviousValueLength,
    EscrowUpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9997b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9997b-110">Parameters</span></span>

  - <span data-ttu-id="9997b-111">sesid</span><span class="sxs-lookup"><span data-stu-id="9997b-111">sesid</span></span>  
    <span data-ttu-id="9997b-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9997b-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9997b-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9997b-113">The session to use.</span></span> <span data-ttu-id="9997b-114">A sessão deve estar em uma transação.</span><span class="sxs-lookup"><span data-stu-id="9997b-114">The session must be in a transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="9997b-115">TableID</span><span class="sxs-lookup"><span data-stu-id="9997b-115">tableid</span></span>  
    <span data-ttu-id="9997b-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9997b-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9997b-117">O cursor a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="9997b-117">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="9997b-118">columnid</span><span class="sxs-lookup"><span data-stu-id="9997b-118">columnid</span></span>  
    <span data-ttu-id="9997b-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9997b-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="9997b-120">A coluna a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="9997b-120">The column to update.</span></span> <span data-ttu-id="9997b-121">Deve ser uma coluna atualizável de caução.</span><span class="sxs-lookup"><span data-stu-id="9997b-121">This must be an escrow updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="9997b-122">delta</span><span class="sxs-lookup"><span data-stu-id="9997b-122">delta</span></span>  
    <span data-ttu-id="9997b-123">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="9997b-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="9997b-124">O buffer que contém o adendo.</span><span class="sxs-lookup"><span data-stu-id="9997b-124">The buffer containing the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="9997b-125">deltaSize</span><span class="sxs-lookup"><span data-stu-id="9997b-125">deltaSize</span></span>  
    <span data-ttu-id="9997b-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9997b-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="9997b-127">O tamanho do adendo.</span><span class="sxs-lookup"><span data-stu-id="9997b-127">The size of the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="9997b-128">anteriorvalue</span><span class="sxs-lookup"><span data-stu-id="9997b-128">previousValue</span></span>  
    <span data-ttu-id="9997b-129">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="9997b-129">Type: \[\]</span></span>  
    
    <span data-ttu-id="9997b-130">Um buffer de saída que receberá o valor atual da coluna.</span><span class="sxs-lookup"><span data-stu-id="9997b-130">An output buffer that will recieve the current value of the column.</span></span> <span data-ttu-id="9997b-131">Esse buffer pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="9997b-131">This buffer can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="9997b-132">previousValueLength</span><span class="sxs-lookup"><span data-stu-id="9997b-132">previousValueLength</span></span>  
    <span data-ttu-id="9997b-133">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9997b-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="9997b-134">O tamanho do buffer anterior.</span><span class="sxs-lookup"><span data-stu-id="9997b-134">The size of the previousValue buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="9997b-135">actualPreviousValueLength</span><span class="sxs-lookup"><span data-stu-id="9997b-135">actualPreviousValueLength</span></span>  
    <span data-ttu-id="9997b-136">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9997b-136">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="9997b-137">Retorna o tamanho real do anteriorvalue.</span><span class="sxs-lookup"><span data-stu-id="9997b-137">Returns the actual size of the previousValue.</span></span>

<!-- end list -->

  - <span data-ttu-id="9997b-138">grbit</span><span class="sxs-lookup"><span data-stu-id="9997b-138">grbit</span></span>  
    <span data-ttu-id="9997b-139">Tipo: [Microsoft. ISAM. ESENT. Interop. EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9997b-139">Type: [Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9997b-140">Opções de atualização de caução.</span><span class="sxs-lookup"><span data-stu-id="9997b-140">Escrow update options.</span></span>

## <a name="see-also"></a><span data-ttu-id="9997b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="9997b-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9997b-142">Referência</span><span class="sxs-lookup"><span data-stu-id="9997b-142">Reference</span></span>

[<span data-ttu-id="9997b-143">Classe de API</span><span class="sxs-lookup"><span data-stu-id="9997b-143">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9997b-144">Membros da API</span><span class="sxs-lookup"><span data-stu-id="9997b-144">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9997b-145">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9997b-145">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
