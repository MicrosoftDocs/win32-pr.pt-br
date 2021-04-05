---
description: 'Saiba mais sobre: método API. JetDelete'
title: Método API. JetDelete
TOCTitle: 'JetDelete method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDelete(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdelete(v=EXCHG.10)
ms:contentKeyID: 55100681
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbc3decf125b8d3f3f1df7228852901cca90aae8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826951"
---
# <a name="apijetdelete-method"></a><span data-ttu-id="a95e3-103">Método API. JetDelete</span><span class="sxs-lookup"><span data-stu-id="a95e3-103">Api.JetDelete method</span></span>

<span data-ttu-id="a95e3-104">Exclui o registro atual em uma tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a95e3-104">Deletes the current record in a database table.</span></span>

<span data-ttu-id="a95e3-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a95e3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a95e3-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a95e3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a95e3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a95e3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDelete ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetDelete(sesid, tableid)
```

``` csharp
public static void JetDelete(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="a95e3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a95e3-108">Parameters</span></span>

  - <span data-ttu-id="a95e3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="a95e3-109">sesid</span></span>  
    <span data-ttu-id="a95e3-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a95e3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a95e3-111">A sessão que abriu o cursor.</span><span class="sxs-lookup"><span data-stu-id="a95e3-111">The session that opened the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="a95e3-112">TableID</span><span class="sxs-lookup"><span data-stu-id="a95e3-112">tableid</span></span>  
    <span data-ttu-id="a95e3-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a95e3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a95e3-114">O cursor em uma tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a95e3-114">The cursor on a database table.</span></span> <span data-ttu-id="a95e3-115">A linha atual será excluída.</span><span class="sxs-lookup"><span data-stu-id="a95e3-115">The current row will be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="a95e3-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a95e3-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a95e3-117">Referência</span><span class="sxs-lookup"><span data-stu-id="a95e3-117">Reference</span></span>

[<span data-ttu-id="a95e3-118">Classe de API</span><span class="sxs-lookup"><span data-stu-id="a95e3-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a95e3-119">Membros da API</span><span class="sxs-lookup"><span data-stu-id="a95e3-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a95e3-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a95e3-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
