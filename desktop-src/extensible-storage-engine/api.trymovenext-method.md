---
description: 'Saiba mais sobre: método API. TryMoveNext'
title: Método API. TryMoveNext
TOCTitle: 'TryMoveNext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveNext(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovenext(v=EXCHG.10)
ms:contentKeyID: 55100887
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveNext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveNext
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b4b4e1f296e5549ba3823f698cdcb5cc9f9f42a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090141"
---
# <a name="apitrymovenext-method"></a><span data-ttu-id="4c567-103">Método API. TryMoveNext</span><span class="sxs-lookup"><span data-stu-id="4c567-103">Api.TryMoveNext method</span></span>

<span data-ttu-id="4c567-104">Tente mover para o próximo registro na tabela.</span><span class="sxs-lookup"><span data-stu-id="4c567-104">Try to move to the next record in the table.</span></span> <span data-ttu-id="4c567-105">Se não houver um próximo registro, isso retornará false, se um erro diferente for encontrado, uma exceção será lançada.</span><span class="sxs-lookup"><span data-stu-id="4c567-105">If there is not a next record this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="4c567-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4c567-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4c567-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4c567-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4c567-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c567-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMoveNext ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveNext(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveNext(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="4c567-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c567-109">Parameters</span></span>

  - <span data-ttu-id="4c567-110">sesid</span><span class="sxs-lookup"><span data-stu-id="4c567-110">sesid</span></span>  
    <span data-ttu-id="4c567-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4c567-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4c567-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4c567-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4c567-113">TableID</span><span class="sxs-lookup"><span data-stu-id="4c567-113">tableid</span></span>  
    <span data-ttu-id="4c567-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4c567-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4c567-115">O cursor a ser posicionado.</span><span class="sxs-lookup"><span data-stu-id="4c567-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4c567-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c567-116">Return value</span></span>

<span data-ttu-id="4c567-117">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4c567-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4c567-118">True se a movimentação tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4c567-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4c567-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c567-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4c567-120">Referência</span><span class="sxs-lookup"><span data-stu-id="4c567-120">Reference</span></span>

[<span data-ttu-id="4c567-121">Classe de API</span><span class="sxs-lookup"><span data-stu-id="4c567-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4c567-122">Membros da API</span><span class="sxs-lookup"><span data-stu-id="4c567-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4c567-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4c567-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
