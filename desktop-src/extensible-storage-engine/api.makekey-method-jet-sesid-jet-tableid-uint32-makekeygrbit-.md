---
description: 'Saiba mais sobre: método API. MakeKey (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)'
title: Método API. MakeKey (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.UInt32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100848
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45edbf959058ccb1c50b82a13f0ca84cdd16a7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763506"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-uint32-makekeygrbit"></a><span data-ttu-id="9625c-103">Método API. MakeKey (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="9625c-103">Api.MakeKey method (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)</span></span>

<span data-ttu-id="9625c-104">Constrói uma chave de pesquisa que pode ser usada por [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) e [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="9625c-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="9625c-105">Esta API não está em conformidade com CLS.</span><span class="sxs-lookup"><span data-stu-id="9625c-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="9625c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9625c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9625c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9625c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9625c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9625c-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As UInteger, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As UInteger
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    uint data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9625c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9625c-109">Parameters</span></span>

  - <span data-ttu-id="9625c-110">sesid</span><span class="sxs-lookup"><span data-stu-id="9625c-110">sesid</span></span>  
    <span data-ttu-id="9625c-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9625c-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9625c-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9625c-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9625c-113">TableID</span><span class="sxs-lookup"><span data-stu-id="9625c-113">tableid</span></span>  
    <span data-ttu-id="9625c-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9625c-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9625c-115">O cursor no qual criar a chave.</span><span class="sxs-lookup"><span data-stu-id="9625c-115">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="9625c-116">data</span><span class="sxs-lookup"><span data-stu-id="9625c-116">data</span></span>  
    <span data-ttu-id="9625c-117">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="9625c-117">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="9625c-118">Dados da coluna para a coluna de chave atual do índice atual.</span><span class="sxs-lookup"><span data-stu-id="9625c-118">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="9625c-119">grbit</span><span class="sxs-lookup"><span data-stu-id="9625c-119">grbit</span></span>  
    <span data-ttu-id="9625c-120">Tipo: [Microsoft. ISAM. ESENT. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9625c-120">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9625c-121">Opções de chave.</span><span class="sxs-lookup"><span data-stu-id="9625c-121">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="9625c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9625c-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9625c-123">Referência</span><span class="sxs-lookup"><span data-stu-id="9625c-123">Reference</span></span>

[<span data-ttu-id="9625c-124">Classe de API</span><span class="sxs-lookup"><span data-stu-id="9625c-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9625c-125">Membros da API</span><span class="sxs-lookup"><span data-stu-id="9625c-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9625c-126">Sobrecarga de MakeKey</span><span class="sxs-lookup"><span data-stu-id="9625c-126">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="9625c-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9625c-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
