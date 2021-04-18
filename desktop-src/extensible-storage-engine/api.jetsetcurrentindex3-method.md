---
description: 'Saiba mais sobre: método API. JetSetCurrentIndex3'
title: Método API. JetSetCurrentIndex3
TOCTitle: 'JetSetCurrentIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex3(v=EXCHG.10)
ms:contentKeyID: 55100805
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c56f259a35026bb47a5e58b7b364b52d9bedbc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751737"
---
# <a name="apijetsetcurrentindex3-method"></a><span data-ttu-id="ba13b-103">Método API. JetSetCurrentIndex3</span><span class="sxs-lookup"><span data-stu-id="ba13b-103">Api.JetSetCurrentIndex3 method</span></span>

<span data-ttu-id="ba13b-104">Define o índice atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="ba13b-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="ba13b-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ba13b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ba13b-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ba13b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ba13b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba13b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex3 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex3(sesid, _
    tableid, index, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex3(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="ba13b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba13b-108">Parameters</span></span>

  - <span data-ttu-id="ba13b-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ba13b-109">sesid</span></span>  
    <span data-ttu-id="ba13b-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ba13b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ba13b-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="ba13b-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ba13b-112">TableID</span><span class="sxs-lookup"><span data-stu-id="ba13b-112">tableid</span></span>  
    <span data-ttu-id="ba13b-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ba13b-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ba13b-114">O cursor no qual definir o índice.</span><span class="sxs-lookup"><span data-stu-id="ba13b-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="ba13b-115">índice</span><span class="sxs-lookup"><span data-stu-id="ba13b-115">index</span></span>  
    <span data-ttu-id="ba13b-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ba13b-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ba13b-117">O nome do índice a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="ba13b-117">The name of the index to be selected.</span></span> <span data-ttu-id="ba13b-118">Se isso for nulo ou vazio, o índice primário será selecionado.</span><span class="sxs-lookup"><span data-stu-id="ba13b-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="ba13b-119">grbit</span><span class="sxs-lookup"><span data-stu-id="ba13b-119">grbit</span></span>  
    <span data-ttu-id="ba13b-120">Tipo: [Microsoft. ISAM. ESENT. Interop. SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ba13b-120">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ba13b-121">Definir opções de índice.</span><span class="sxs-lookup"><span data-stu-id="ba13b-121">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="ba13b-122">itagSequence</span><span class="sxs-lookup"><span data-stu-id="ba13b-122">itagSequence</span></span>  
    <span data-ttu-id="ba13b-123">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ba13b-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ba13b-124">Número de sequência do valor de coluna com valores múltiplos que será usado para posicionar o cursor no novo índice.</span><span class="sxs-lookup"><span data-stu-id="ba13b-124">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="ba13b-125">Esse parâmetro só é usado em conjunto com [nomove](./setcurrentindexgrbit-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="ba13b-125">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="ba13b-126">Quando esse parâmetro não estiver presente ou estiver definido como zero, seu valor será presumido como 1.</span><span class="sxs-lookup"><span data-stu-id="ba13b-126">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba13b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba13b-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ba13b-128">Referência</span><span class="sxs-lookup"><span data-stu-id="ba13b-128">Reference</span></span>

[<span data-ttu-id="ba13b-129">Classe de API</span><span class="sxs-lookup"><span data-stu-id="ba13b-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ba13b-130">Membros da API</span><span class="sxs-lookup"><span data-stu-id="ba13b-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ba13b-131">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ba13b-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
