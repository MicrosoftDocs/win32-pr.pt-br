---
description: 'Saiba mais sobre: método API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)'
title: Método API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100801
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f52c900521d28c82245db53b98ab376dd82faec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811559"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-setcolumngrbit-jet_setinfo"></a><span data-ttu-id="3417e-103">Método API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)</span><span class="sxs-lookup"><span data-stu-id="3417e-103">Api.JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)</span></span>

<span data-ttu-id="3417e-104">A função JetSetColumn modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</span><span class="sxs-lookup"><span data-stu-id="3417e-104">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="3417e-105">Ele pode substituir um valor existente, adicionar um novo valor a uma sequência de valores em uma coluna com vários valores, remover um valor de uma sequência de valores em uma coluna com vários valores ou atualizar todo ou parte de um valor longo (uma coluna do tipo [LONGTEXT](./jet-coltyp-enumeration.md) ou [LongBinary](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="3417e-105">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type [LongText](./jet-coltyp-enumeration.md) or [LongBinary](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="3417e-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3417e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3417e-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3417e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3417e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3417e-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="3417e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3417e-109">Parameters</span></span>

  - <span data-ttu-id="3417e-110">sesid</span><span class="sxs-lookup"><span data-stu-id="3417e-110">sesid</span></span>  
    <span data-ttu-id="3417e-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3417e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3417e-112">A sessão que está executando a atualização.</span><span class="sxs-lookup"><span data-stu-id="3417e-112">The session which is performing the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="3417e-113">TableID</span><span class="sxs-lookup"><span data-stu-id="3417e-113">tableid</span></span>  
    <span data-ttu-id="3417e-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3417e-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3417e-115">O cursor a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="3417e-115">The cursor to update.</span></span> <span data-ttu-id="3417e-116">Uma atualização deve ser preparada.</span><span class="sxs-lookup"><span data-stu-id="3417e-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="3417e-117">columnid</span><span class="sxs-lookup"><span data-stu-id="3417e-117">columnid</span></span>  
    <span data-ttu-id="3417e-118">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3417e-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="3417e-119">O columnid a ser definido.</span><span class="sxs-lookup"><span data-stu-id="3417e-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="3417e-120">data</span><span class="sxs-lookup"><span data-stu-id="3417e-120">data</span></span>  
    <span data-ttu-id="3417e-121">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="3417e-121">Type: \[\]</span></span>  
    
    <span data-ttu-id="3417e-122">Os dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="3417e-122">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="3417e-123">dataSize</span><span class="sxs-lookup"><span data-stu-id="3417e-123">dataSize</span></span>  
    <span data-ttu-id="3417e-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3417e-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3417e-125">O tamanho dos dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="3417e-125">The size of data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="3417e-126">dataOffset</span><span class="sxs-lookup"><span data-stu-id="3417e-126">dataOffset</span></span>  
    <span data-ttu-id="3417e-127">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3417e-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3417e-128">O deslocamento no buffer de dados do qual definir dados.</span><span class="sxs-lookup"><span data-stu-id="3417e-128">The offset in the data buffer to set data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="3417e-129">grbit</span><span class="sxs-lookup"><span data-stu-id="3417e-129">grbit</span></span>  
    <span data-ttu-id="3417e-130">Tipo: [Microsoft. ISAM. ESENT. Interop. SetColumnGrbit](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3417e-130">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3417e-131">Opções SetColumn.</span><span class="sxs-lookup"><span data-stu-id="3417e-131">SetColumn options.</span></span>

<!-- end list -->

  - <span data-ttu-id="3417e-132">setinfo</span><span class="sxs-lookup"><span data-stu-id="3417e-132">setinfo</span></span>  
    <span data-ttu-id="3417e-133">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SETINFO](./jet-setinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="3417e-133">Type: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span></span>  
    
    <span data-ttu-id="3417e-134">Usado para especificar ITAG ou deslocamento de valor longo.</span><span class="sxs-lookup"><span data-stu-id="3417e-134">Used to specify itag or long-value offset.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3417e-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3417e-135">Return value</span></span>

<span data-ttu-id="3417e-136">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3417e-136">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="3417e-137">Um valor de aviso.</span><span class="sxs-lookup"><span data-stu-id="3417e-137">A warning value.</span></span>  

## <a name="remarks"></a><span data-ttu-id="3417e-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="3417e-138">Remarks</span></span>

<span data-ttu-id="3417e-139">Essa é uma versão somente interna da API que usa um buffer de dados e um deslocamento no buffer.</span><span class="sxs-lookup"><span data-stu-id="3417e-139">This is an internal-only version of the API that takes a data buffer and an offset into the buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="3417e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3417e-140">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3417e-141">Referência</span><span class="sxs-lookup"><span data-stu-id="3417e-141">Reference</span></span>

[<span data-ttu-id="3417e-142">Classe de API</span><span class="sxs-lookup"><span data-stu-id="3417e-142">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3417e-143">Membros da API</span><span class="sxs-lookup"><span data-stu-id="3417e-143">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3417e-144">Sobrecarga de JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="3417e-144">JetSetColumn overload</span></span>](./api.jetsetcolumn-method.md)

[<span data-ttu-id="3417e-145">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3417e-145">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
