---
description: 'Saiba mais sobre: método API. JetSetIndexRange'
title: Método API. JetSetIndexRange
TOCTitle: 'JetSetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100817
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ad13e04674de60aa1c0f55cf4cd4570f8b7ddaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010412"
---
# <a name="apijetsetindexrange-method"></a><span data-ttu-id="13f86-103">Método API. JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="13f86-103">Api.JetSetIndexRange method</span></span>

<span data-ttu-id="13f86-104">Limita temporariamente o conjunto de entradas de índice que o cursor pode percorrer usando [JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) para aqueles que começam da entrada de índice atual e terminam na entrada de índice que corresponde aos critérios de pesquisa especificados pela chave de pesquisa no cursor e nos critérios de associação especificados.</span><span class="sxs-lookup"><span data-stu-id="13f86-104">Temporarily limits the set of index entries that the cursor can walk using [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="13f86-105">Uma chave de pesquisa deve ter sido construída anteriormente usando [JetMakeKey (JET_SESID, JET_TABLEID, \[ \] , Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="13f86-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="13f86-106">Consulte também [TrySetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="13f86-106">Also see [TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span></span>

<span data-ttu-id="13f86-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="13f86-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="13f86-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="13f86-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="13f86-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13f86-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbitApi.JetSetIndexRange(sesid, tableid, _
    grbit)
```

``` csharp
public static void JetSetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="13f86-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13f86-110">Parameters</span></span>

  - <span data-ttu-id="13f86-111">sesid</span><span class="sxs-lookup"><span data-stu-id="13f86-111">sesid</span></span>  
    <span data-ttu-id="13f86-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="13f86-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="13f86-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="13f86-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="13f86-114">TableID</span><span class="sxs-lookup"><span data-stu-id="13f86-114">tableid</span></span>  
    <span data-ttu-id="13f86-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="13f86-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="13f86-116">O cursor no qual definir o intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="13f86-116">The cursor to set the index range on.</span></span>

<!-- end list -->

  - <span data-ttu-id="13f86-117">grbit</span><span class="sxs-lookup"><span data-stu-id="13f86-117">grbit</span></span>  
    <span data-ttu-id="13f86-118">Tipo: [Microsoft. ISAM. ESENT. Interop. SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="13f86-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="13f86-119">Opções de intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="13f86-119">Index range options.</span></span>

## <a name="see-also"></a><span data-ttu-id="13f86-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="13f86-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="13f86-121">Referência</span><span class="sxs-lookup"><span data-stu-id="13f86-121">Reference</span></span>

[<span data-ttu-id="13f86-122">Classe de API</span><span class="sxs-lookup"><span data-stu-id="13f86-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="13f86-123">Membros da API</span><span class="sxs-lookup"><span data-stu-id="13f86-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="13f86-124">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="13f86-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
