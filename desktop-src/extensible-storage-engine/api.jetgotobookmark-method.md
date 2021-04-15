---
description: 'Saiba mais sobre: método API. JetGotoBookmark'
title: Método API. JetGotoBookmark
TOCTitle: 'JetGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55100753
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 362a174e3da4dad864fd504e1678b4a3a1477e1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506244"
---
# <a name="apijetgotobookmark-method"></a><span data-ttu-id="391f4-103">Método API. JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="391f4-103">Api.JetGotoBookmark method</span></span>

<span data-ttu-id="391f4-104">Posiciona um cursor para uma entrada de índice para o registro que está associado ao indicador especificado.</span><span class="sxs-lookup"><span data-stu-id="391f4-104">Positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="391f4-105">O indicador pode ser usado com qualquer índice definido em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="391f4-105">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="391f4-106">O indicador de um registro pode ser recuperado usando [JetGetBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetgetbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="391f4-106">The bookmark for a record can be retrieved using [JetGetBookmark(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetgetbookmark-method.md).</span></span>

<span data-ttu-id="391f4-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="391f4-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="391f4-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="391f4-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="391f4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="391f4-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As IntegerApi.JetGotoBookmark(sesid, tableid, _
    bookmark, bookmarkSize)
```

``` csharp
public static void JetGotoBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="391f4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="391f4-110">Parameters</span></span>

  - <span data-ttu-id="391f4-111">sesid</span><span class="sxs-lookup"><span data-stu-id="391f4-111">sesid</span></span>  
    <span data-ttu-id="391f4-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="391f4-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="391f4-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="391f4-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="391f4-114">TableID</span><span class="sxs-lookup"><span data-stu-id="391f4-114">tableid</span></span>  
    <span data-ttu-id="391f4-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="391f4-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="391f4-116">O cursor a ser posicionado.</span><span class="sxs-lookup"><span data-stu-id="391f4-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="391f4-117">indicador</span><span class="sxs-lookup"><span data-stu-id="391f4-117">bookmark</span></span>  
    <span data-ttu-id="391f4-118">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="391f4-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="391f4-119">O indicador usado para posicionar o cursor.</span><span class="sxs-lookup"><span data-stu-id="391f4-119">The bookmark used to position the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="391f4-120">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="391f4-120">bookmarkSize</span></span>  
    <span data-ttu-id="391f4-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="391f4-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="391f4-122">O tamanho do indicador.</span><span class="sxs-lookup"><span data-stu-id="391f4-122">The size of the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="391f4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="391f4-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="391f4-124">Referência</span><span class="sxs-lookup"><span data-stu-id="391f4-124">Reference</span></span>

[<span data-ttu-id="391f4-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="391f4-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="391f4-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="391f4-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="391f4-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="391f4-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
