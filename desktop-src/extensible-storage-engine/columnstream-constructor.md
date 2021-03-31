---
description: 'Saiba mais sobre: Construtor ColumnStream'
title: Construtor ColumnStream
TOCTitle: 'ColumnStream constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 498fed2daf2cad5903d9597689a80eadca7bd569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921137"
---
# <a name="columnstream-constructor"></a><span data-ttu-id="705dd-103">Construtor ColumnStream</span><span class="sxs-lookup"><span data-stu-id="705dd-103">ColumnStream constructor</span></span>

<span data-ttu-id="705dd-104">Inicializa uma nova instância da classe ColumnStream.</span><span class="sxs-lookup"><span data-stu-id="705dd-104">Initializes a new instance of the ColumnStream class.</span></span>

<span data-ttu-id="705dd-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="705dd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="705dd-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="705dd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="705dd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="705dd-107">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID

Dim instance As New ColumnStream(sesid, tableid, _
    columnid)
```

``` csharp
public ColumnStream(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="705dd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="705dd-108">Parameters</span></span>

  - <span data-ttu-id="705dd-109">sesid</span><span class="sxs-lookup"><span data-stu-id="705dd-109">sesid</span></span>  
    <span data-ttu-id="705dd-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="705dd-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="705dd-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="705dd-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="705dd-112">TableID</span><span class="sxs-lookup"><span data-stu-id="705dd-112">tableid</span></span>  
    <span data-ttu-id="705dd-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="705dd-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="705dd-114">O cursor a ser usado.</span><span class="sxs-lookup"><span data-stu-id="705dd-114">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="705dd-115">columnid</span><span class="sxs-lookup"><span data-stu-id="705dd-115">columnid</span></span>  
    <span data-ttu-id="705dd-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="705dd-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="705dd-117">O columnid da coluna da qual definir/recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="705dd-117">The columnid of the column to set/retrieve data from.</span></span>

## <a name="see-also"></a><span data-ttu-id="705dd-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="705dd-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="705dd-119">Referência</span><span class="sxs-lookup"><span data-stu-id="705dd-119">Reference</span></span>

[<span data-ttu-id="705dd-120">Classe ColumnStream</span><span class="sxs-lookup"><span data-stu-id="705dd-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="705dd-121">Membros do ColumnStream</span><span class="sxs-lookup"><span data-stu-id="705dd-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="705dd-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="705dd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
