---
description: 'Saiba mais sobre: método API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, SetColumnGrbit, JET_SETINFO)'
title: Método API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, SetColumnGrbit, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100804
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5afebba00c784abf5bf71ac0f524376bd0f3b066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793966"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-setcolumngrbit-jet_setinfo"></a><span data-ttu-id="ff11b-103">Método API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, SetColumnGrbit, JET_SETINFO)</span><span class="sxs-lookup"><span data-stu-id="ff11b-103">Api.JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)</span></span>

<span data-ttu-id="ff11b-104">A função JetSetColumn modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</span><span class="sxs-lookup"><span data-stu-id="ff11b-104">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="ff11b-105">Ele pode substituir um valor existente, adicionar um novo valor a uma sequência de valores em uma coluna com vários valores, remover um valor de uma sequência de valores em uma coluna com vários valores ou atualizar todo ou parte de um valor longo (uma coluna do tipo [LONGTEXT](./jet-coltyp-enumeration.md) ou [LongBinary](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="ff11b-105">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type [LongText](./jet-coltyp-enumeration.md) or [LongBinary](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="ff11b-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ff11b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ff11b-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ff11b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ff11b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff11b-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="ff11b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff11b-109">Parameters</span></span>

  - <span data-ttu-id="ff11b-110">sesid</span><span class="sxs-lookup"><span data-stu-id="ff11b-110">sesid</span></span>  
    <span data-ttu-id="ff11b-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff11b-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ff11b-112">A sessão que está executando a atualização.</span><span class="sxs-lookup"><span data-stu-id="ff11b-112">The session which is performing the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff11b-113">TableID</span><span class="sxs-lookup"><span data-stu-id="ff11b-113">tableid</span></span>  
    <span data-ttu-id="ff11b-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff11b-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ff11b-115">O cursor a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="ff11b-115">The cursor to update.</span></span> <span data-ttu-id="ff11b-116">Uma atualização deve ser preparada.</span><span class="sxs-lookup"><span data-stu-id="ff11b-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff11b-117">columnid</span><span class="sxs-lookup"><span data-stu-id="ff11b-117">columnid</span></span>  
    <span data-ttu-id="ff11b-118">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff11b-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="ff11b-119">O columnid a ser definido.</span><span class="sxs-lookup"><span data-stu-id="ff11b-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff11b-120">data</span><span class="sxs-lookup"><span data-stu-id="ff11b-120">data</span></span>  
    <span data-ttu-id="ff11b-121">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="ff11b-121">Type: \[\]</span></span>  
    
    <span data-ttu-id="ff11b-122">Os dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="ff11b-122">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff11b-123">dataSize</span><span class="sxs-lookup"><span data-stu-id="ff11b-123">dataSize</span></span>  
    <span data-ttu-id="ff11b-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ff11b-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ff11b-125">O tamanho dos dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="ff11b-125">The size of data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff11b-126">grbit</span><span class="sxs-lookup"><span data-stu-id="ff11b-126">grbit</span></span>  
    <span data-ttu-id="ff11b-127">Tipo: [Microsoft. ISAM. ESENT. Interop. SetColumnGrbit](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ff11b-127">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ff11b-128">Opções SetColumn.</span><span class="sxs-lookup"><span data-stu-id="ff11b-128">SetColumn options.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff11b-129">setinfo</span><span class="sxs-lookup"><span data-stu-id="ff11b-129">setinfo</span></span>  
    <span data-ttu-id="ff11b-130">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SETINFO](./jet-setinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="ff11b-130">Type: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span></span>  
    
    <span data-ttu-id="ff11b-131">Usado para especificar ITAG ou deslocamento de valor longo.</span><span class="sxs-lookup"><span data-stu-id="ff11b-131">Used to specify itag or long-value offset.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ff11b-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff11b-132">Return value</span></span>

<span data-ttu-id="ff11b-133">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ff11b-133">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="ff11b-134">Um código de aviso.</span><span class="sxs-lookup"><span data-stu-id="ff11b-134">A warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="ff11b-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff11b-135">Remarks</span></span>

<span data-ttu-id="ff11b-136">Os métodos SetColumn fornecem substituições específicas de DataType que podem ser mais eficientes.</span><span class="sxs-lookup"><span data-stu-id="ff11b-136">The SetColumn methods provide datatype-specific overrides which may be more efficient.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff11b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff11b-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ff11b-138">Referência</span><span class="sxs-lookup"><span data-stu-id="ff11b-138">Reference</span></span>

[<span data-ttu-id="ff11b-139">Classe de API</span><span class="sxs-lookup"><span data-stu-id="ff11b-139">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ff11b-140">Membros da API</span><span class="sxs-lookup"><span data-stu-id="ff11b-140">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ff11b-141">Sobrecarga de JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="ff11b-141">JetSetColumn overload</span></span>](./api.jetsetcolumn-method.md)

[<span data-ttu-id="ff11b-142">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ff11b-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
