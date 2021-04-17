---
description: 'Saiba mais sobre: método API. JetSetCurrentIndex4'
title: Método API. JetSetCurrentIndex4
TOCTitle: 'JetSetCurrentIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex4(v=EXCHG.10)
ms:contentKeyID: 55100806
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2b9319554b998175b3f533c6cd5f4c2d05ba02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759277"
---
# <a name="apijetsetcurrentindex4-method"></a><span data-ttu-id="8596b-103">Método API. JetSetCurrentIndex4</span><span class="sxs-lookup"><span data-stu-id="8596b-103">Api.JetSetCurrentIndex4 method</span></span>

<span data-ttu-id="8596b-104">Define o índice atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="8596b-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="8596b-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8596b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8596b-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8596b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8596b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8596b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    indexid As JET_INDEXID, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim indexid As JET_INDEXID
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex4(sesid, _
    tableid, index, indexid, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    JET_INDEXID indexid,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="8596b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8596b-108">Parameters</span></span>

  - <span data-ttu-id="8596b-109">sesid</span><span class="sxs-lookup"><span data-stu-id="8596b-109">sesid</span></span>  
    <span data-ttu-id="8596b-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8596b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8596b-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="8596b-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8596b-112">TableID</span><span class="sxs-lookup"><span data-stu-id="8596b-112">tableid</span></span>  
    <span data-ttu-id="8596b-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8596b-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8596b-114">O cursor no qual definir o índice.</span><span class="sxs-lookup"><span data-stu-id="8596b-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="8596b-115">índice</span><span class="sxs-lookup"><span data-stu-id="8596b-115">index</span></span>  
    <span data-ttu-id="8596b-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8596b-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8596b-117">O nome do índice a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="8596b-117">The name of the index to be selected.</span></span> <span data-ttu-id="8596b-118">Se isso for nulo ou vazio, o índice primário será selecionado.</span><span class="sxs-lookup"><span data-stu-id="8596b-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="8596b-119">indexid</span><span class="sxs-lookup"><span data-stu-id="8596b-119">indexid</span></span>  
    <span data-ttu-id="8596b-120">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="8596b-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="8596b-121">A ID do índice a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="8596b-121">The id of the index to select.</span></span> <span data-ttu-id="8596b-122">Essa ID pode ser obtida usando JetGetIndexInfo ou JetGetTableIndexInfo com a opção [IndexID](./jet-idxinfo-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="8596b-122">This id can be obtained using JetGetIndexInfo or JetGetTableIndexInfo with the [IndexId](./jet-idxinfo-enumeration.md) option.</span></span>

<!-- end list -->

  - <span data-ttu-id="8596b-123">grbit</span><span class="sxs-lookup"><span data-stu-id="8596b-123">grbit</span></span>  
    <span data-ttu-id="8596b-124">Tipo: [Microsoft. ISAM. ESENT. Interop. SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8596b-124">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8596b-125">Definir opções de índice.</span><span class="sxs-lookup"><span data-stu-id="8596b-125">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="8596b-126">itagSequence</span><span class="sxs-lookup"><span data-stu-id="8596b-126">itagSequence</span></span>  
    <span data-ttu-id="8596b-127">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8596b-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8596b-128">Número de sequência do valor de coluna com valores múltiplos que será usado para posicionar o cursor no novo índice.</span><span class="sxs-lookup"><span data-stu-id="8596b-128">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="8596b-129">Esse parâmetro só é usado em conjunto com [nomove](./setcurrentindexgrbit-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="8596b-129">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="8596b-130">Quando esse parâmetro não estiver presente ou estiver definido como zero, seu valor será presumido como 1.</span><span class="sxs-lookup"><span data-stu-id="8596b-130">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="8596b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8596b-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8596b-132">Referência</span><span class="sxs-lookup"><span data-stu-id="8596b-132">Reference</span></span>

[<span data-ttu-id="8596b-133">Classe de API</span><span class="sxs-lookup"><span data-stu-id="8596b-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8596b-134">Membros da API</span><span class="sxs-lookup"><span data-stu-id="8596b-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8596b-135">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8596b-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
