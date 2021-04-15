---
description: 'Saiba mais sobre: método API. JetDupCursor'
title: Método API. JetDupCursor
TOCTitle: 'JetDupCursor method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupCursor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.DupCursorGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupcursor(v=EXCHG.10)
ms:contentKeyID: 55100686
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fce19d23838f3dfeab5317bfa7ea1aaacfcb508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501515"
---
# <a name="apijetdupcursor-method"></a><span data-ttu-id="54dee-103">Método API. JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="54dee-103">Api.JetDupCursor method</span></span>

<span data-ttu-id="54dee-104">Duplica um cursor Open e retorna um identificador para o cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="54dee-104">Duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="54dee-105">Se o cursor que foi duplicado era um cursor somente leitura, o cursor duplicado também é um cursor somente leitura.</span><span class="sxs-lookup"><span data-stu-id="54dee-105">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="54dee-106">Qualquer estado relacionado à construção de uma chave de pesquisa ou à atualização de um registro não é copiado para o cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="54dee-106">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="54dee-107">Além disso, o local do cursor original não é duplicado no cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="54dee-107">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="54dee-108">O cursor duplicado sempre é aberto no índice clusterizado e seu local está sempre na primeira linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="54dee-108">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

<span data-ttu-id="54dee-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="54dee-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="54dee-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="54dee-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="54dee-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54dee-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupCursor ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef newTableid As JET_TABLEID, _
    grbit As DupCursorGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim newTableid As JET_TABLEID
Dim grbit As DupCursorGrbitApi.JetDupCursor(sesid, tableid, _
    newTableid, grbit)
```

``` csharp
public static void JetDupCursor(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_TABLEID newTableid,
    DupCursorGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="54dee-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54dee-112">Parameters</span></span>

  - <span data-ttu-id="54dee-113">sesid</span><span class="sxs-lookup"><span data-stu-id="54dee-113">sesid</span></span>  
    <span data-ttu-id="54dee-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="54dee-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="54dee-115">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="54dee-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="54dee-116">TableID</span><span class="sxs-lookup"><span data-stu-id="54dee-116">tableid</span></span>  
    <span data-ttu-id="54dee-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="54dee-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="54dee-118">O cursor para duplicar.</span><span class="sxs-lookup"><span data-stu-id="54dee-118">The cursor to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="54dee-119">newTableid</span><span class="sxs-lookup"><span data-stu-id="54dee-119">newTableid</span></span>  
    <span data-ttu-id="54dee-120">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="54dee-120">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="54dee-121">O cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="54dee-121">The duplicated cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="54dee-122">grbit</span><span class="sxs-lookup"><span data-stu-id="54dee-122">grbit</span></span>  
    <span data-ttu-id="54dee-123">Tipo: [Microsoft. ISAM. ESENT. Interop. DupCursorGrbit](./dupcursorgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="54dee-123">Type: [Microsoft.Isam.Esent.Interop.DupCursorGrbit](./dupcursorgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="54dee-124">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="54dee-124">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="54dee-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="54dee-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="54dee-126">Referência</span><span class="sxs-lookup"><span data-stu-id="54dee-126">Reference</span></span>

[<span data-ttu-id="54dee-127">Classe de API</span><span class="sxs-lookup"><span data-stu-id="54dee-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="54dee-128">Membros da API</span><span class="sxs-lookup"><span data-stu-id="54dee-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="54dee-129">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="54dee-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
