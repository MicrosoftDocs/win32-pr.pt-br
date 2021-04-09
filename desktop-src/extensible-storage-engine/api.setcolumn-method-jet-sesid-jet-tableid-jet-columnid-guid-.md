---
description: 'Saiba mais sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, GUID)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, GUID)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Guid)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Guid)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100874
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 105b516b46cde52149da4b1a48b99ab931ede85c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010338"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-guid"></a><span data-ttu-id="e2fbe-103">Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, GUID)</span><span class="sxs-lookup"><span data-stu-id="e2fbe-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Guid)</span></span>

<span data-ttu-id="e2fbe-104">Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</span><span class="sxs-lookup"><span data-stu-id="e2fbe-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="e2fbe-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2fbe-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2fbe-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2fbe-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2fbe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2fbe-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Guid _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As GuidApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Guid data
)
```

#### <a name="parameters"></a><span data-ttu-id="e2fbe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2fbe-108">Parameters</span></span>

  - <span data-ttu-id="e2fbe-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e2fbe-109">sesid</span></span>  
    <span data-ttu-id="e2fbe-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e2fbe-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e2fbe-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e2fbe-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2fbe-112">TableID</span><span class="sxs-lookup"><span data-stu-id="e2fbe-112">tableid</span></span>  
    <span data-ttu-id="e2fbe-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e2fbe-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e2fbe-114">O cursor a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="e2fbe-114">The cursor to update.</span></span> <span data-ttu-id="e2fbe-115">Uma atualização deve ser preparada.</span><span class="sxs-lookup"><span data-stu-id="e2fbe-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2fbe-116">columnid</span><span class="sxs-lookup"><span data-stu-id="e2fbe-116">columnid</span></span>  
    <span data-ttu-id="e2fbe-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e2fbe-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e2fbe-118">O columnid a ser definido.</span><span class="sxs-lookup"><span data-stu-id="e2fbe-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2fbe-119">data</span><span class="sxs-lookup"><span data-stu-id="e2fbe-119">data</span></span>  
    <span data-ttu-id="e2fbe-120">Tipo: [System. GUID](/dotnet/api/system.guid)</span><span class="sxs-lookup"><span data-stu-id="e2fbe-120">Type: [System.Guid](/dotnet/api/system.guid)</span></span>  
    
    <span data-ttu-id="e2fbe-121">Os dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="e2fbe-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2fbe-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2fbe-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2fbe-123">Referência</span><span class="sxs-lookup"><span data-stu-id="e2fbe-123">Reference</span></span>

[<span data-ttu-id="e2fbe-124">Classe de API</span><span class="sxs-lookup"><span data-stu-id="e2fbe-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e2fbe-125">Membros da API</span><span class="sxs-lookup"><span data-stu-id="e2fbe-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e2fbe-126">Sobrecarga de SetColumn</span><span class="sxs-lookup"><span data-stu-id="e2fbe-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="e2fbe-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e2fbe-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
