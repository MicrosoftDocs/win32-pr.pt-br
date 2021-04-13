---
description: 'Saiba mais sobre: método API. JetGetRecordPosition'
title: Método API. JetGetRecordPosition
TOCTitle: 'JetGetRecordPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetrecordposition(v=EXCHG.10)
ms:contentKeyID: 55100722
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00350853172d784c270c197e7c58ad6fa616560f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501507"
---
# <a name="apijetgetrecordposition-method"></a><span data-ttu-id="95c64-103">Método API. JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="95c64-103">Api.JetGetRecordPosition method</span></span>

<span data-ttu-id="95c64-104">Retorna a posição fracionária do registro atual no índice atual na forma de uma estrutura de [JET_RECPOS](./jet-recpos-class.md) .</span><span class="sxs-lookup"><span data-stu-id="95c64-104">Returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-class.md) structure.</span></span> <span data-ttu-id="95c64-105">Consulte também [JetGotoPosition (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).</span><span class="sxs-lookup"><span data-stu-id="95c64-105">Also see [JetGotoPosition(JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).</span></span>

<span data-ttu-id="95c64-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="95c64-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="95c64-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="95c64-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="95c64-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95c64-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetRecordPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGetRecordPosition(sesid, _
    tableid, recpos)
```

``` csharp
public static void JetGetRecordPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_RECPOS recpos
)
```

#### <a name="parameters"></a><span data-ttu-id="95c64-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95c64-109">Parameters</span></span>

  - <span data-ttu-id="95c64-110">sesid</span><span class="sxs-lookup"><span data-stu-id="95c64-110">sesid</span></span>  
    <span data-ttu-id="95c64-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="95c64-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="95c64-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="95c64-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="95c64-113">TableID</span><span class="sxs-lookup"><span data-stu-id="95c64-113">tableid</span></span>  
    <span data-ttu-id="95c64-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="95c64-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="95c64-115">O cursor posicionado no registro.</span><span class="sxs-lookup"><span data-stu-id="95c64-115">The cursor positioned on the record.</span></span>

<!-- end list -->

  - <span data-ttu-id="95c64-116">recpos</span><span class="sxs-lookup"><span data-stu-id="95c64-116">recpos</span></span>  
    <span data-ttu-id="95c64-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RECPOS](./jet-recpos-class.md)</span><span class="sxs-lookup"><span data-stu-id="95c64-117">Type: [Microsoft.Isam.Esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span></span>  
    
    <span data-ttu-id="95c64-118">Retorna a posição fracionária aproximada do registro.</span><span class="sxs-lookup"><span data-stu-id="95c64-118">Returns the approximate fractional position of the record.</span></span>

## <a name="see-also"></a><span data-ttu-id="95c64-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="95c64-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="95c64-120">Referência</span><span class="sxs-lookup"><span data-stu-id="95c64-120">Reference</span></span>

[<span data-ttu-id="95c64-121">Classe de API</span><span class="sxs-lookup"><span data-stu-id="95c64-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="95c64-122">Membros da API</span><span class="sxs-lookup"><span data-stu-id="95c64-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="95c64-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="95c64-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
