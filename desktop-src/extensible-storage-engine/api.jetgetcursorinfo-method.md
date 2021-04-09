---
description: 'Saiba mais sobre: método API. JetGetCursorInfo'
title: Método API. JetGetCursorInfo
TOCTitle: 'JetGetCursorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcursorinfo(v=EXCHG.10)
ms:contentKeyID: 55100707
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7144283a062b0097d6866e74d1c263bb130c5e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010420"
---
# <a name="apijetgetcursorinfo-method"></a><span data-ttu-id="acfb6-103">Método API. JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="acfb6-103">Api.JetGetCursorInfo method</span></span>

<span data-ttu-id="acfb6-104">Determine se uma atualização do registro atual de um cursor resultará em um conflito de gravação, com base no status de atualização atual do registro.</span><span class="sxs-lookup"><span data-stu-id="acfb6-104">Determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="acfb6-105">É possível que um conflito de gravação será retornado, mesmo se JetGetCursorInfo retornar com êxito.</span><span class="sxs-lookup"><span data-stu-id="acfb6-105">It is possible that a write conflict will ultimately be returned even if JetGetCursorInfo returns successfully.</span></span> <span data-ttu-id="acfb6-106">Porque outra sessão pode atualizar o registro antes que a sessão atual seja capaz de atualizar o mesmo registro.</span><span class="sxs-lookup"><span data-stu-id="acfb6-106">because another session may update the record before the current session is able to update the same record.</span></span>

<span data-ttu-id="acfb6-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="acfb6-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="acfb6-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="acfb6-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="acfb6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acfb6-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCursorInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetGetCursorInfo(sesid, tableid)
```

``` csharp
public static void JetGetCursorInfo(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="acfb6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acfb6-110">Parameters</span></span>

  - <span data-ttu-id="acfb6-111">sesid</span><span class="sxs-lookup"><span data-stu-id="acfb6-111">sesid</span></span>  
    <span data-ttu-id="acfb6-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="acfb6-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="acfb6-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="acfb6-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="acfb6-114">TableID</span><span class="sxs-lookup"><span data-stu-id="acfb6-114">tableid</span></span>  
    <span data-ttu-id="acfb6-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="acfb6-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="acfb6-116">O cursor a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="acfb6-116">The cursor to check.</span></span>

## <a name="see-also"></a><span data-ttu-id="acfb6-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="acfb6-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="acfb6-118">Referência</span><span class="sxs-lookup"><span data-stu-id="acfb6-118">Reference</span></span>

[<span data-ttu-id="acfb6-119">Classe de API</span><span class="sxs-lookup"><span data-stu-id="acfb6-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="acfb6-120">Membros da API</span><span class="sxs-lookup"><span data-stu-id="acfb6-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="acfb6-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="acfb6-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
