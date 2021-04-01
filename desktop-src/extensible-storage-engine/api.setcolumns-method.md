---
description: 'Saiba mais sobre: método API. SetColumns'
title: Método API. SetColumns
TOCTitle: 'SetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumns(v=EXCHG.10)
ms:contentKeyID: 55100936
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4ed75c668c0000c1d01d521a57ead46055bc8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646643"
---
# <a name="apisetcolumns-method"></a><span data-ttu-id="090c3-103">Método API. SetColumns</span><span class="sxs-lookup"><span data-stu-id="090c3-103">Api.SetColumns method</span></span>

<span data-ttu-id="090c3-104">Define colunas de objetos Columnvalue.</span><span class="sxs-lookup"><span data-stu-id="090c3-104">Sets columns from ColumnValue objects.</span></span>

<span data-ttu-id="090c3-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="090c3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="090c3-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="090c3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="090c3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="090c3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.SetColumns(sesid, tableid, values)
```

``` csharp
public static void SetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="090c3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="090c3-108">Parameters</span></span>

  - <span data-ttu-id="090c3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="090c3-109">sesid</span></span>  
    <span data-ttu-id="090c3-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="090c3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="090c3-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="090c3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="090c3-112">TableID</span><span class="sxs-lookup"><span data-stu-id="090c3-112">tableid</span></span>  
    <span data-ttu-id="090c3-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="090c3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="090c3-114">O cursor a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="090c3-114">The cursor to update.</span></span> <span data-ttu-id="090c3-115">Uma atualização deve ser preparada.</span><span class="sxs-lookup"><span data-stu-id="090c3-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="090c3-116">valores</span><span class="sxs-lookup"><span data-stu-id="090c3-116">values</span></span>  
    <span data-ttu-id="090c3-117">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="090c3-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="090c3-118">Os valores a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="090c3-118">The values to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="090c3-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="090c3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="090c3-120">Referência</span><span class="sxs-lookup"><span data-stu-id="090c3-120">Reference</span></span>

[<span data-ttu-id="090c3-121">Classe de API</span><span class="sxs-lookup"><span data-stu-id="090c3-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="090c3-122">Membros da API</span><span class="sxs-lookup"><span data-stu-id="090c3-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="090c3-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="090c3-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
