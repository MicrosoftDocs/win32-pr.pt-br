---
description: 'Saiba mais sobre: método API. JetRenameColumn'
title: Método API. JetRenameColumn
TOCTitle: 'JetRenameColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRenameColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.String,Microsoft.Isam.Esent.Interop.RenameColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrenamecolumn(v=EXCHG.10)
ms:contentKeyID: 55100786
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRenameColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRenameColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 007bce82d8749611f0fe2b0eae28b54ddedab98f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663238"
---
# <a name="apijetrenamecolumn-method"></a><span data-ttu-id="eb19c-103">Método API. JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="eb19c-103">Api.JetRenameColumn method</span></span>

<span data-ttu-id="eb19c-104">Altera o nome de uma coluna existente.</span><span class="sxs-lookup"><span data-stu-id="eb19c-104">Changes the name of an existing column.</span></span>

<span data-ttu-id="eb19c-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eb19c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eb19c-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eb19c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eb19c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb19c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRenameColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    name As String, _
    newName As String, _
    grbit As RenameColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim name As String
Dim newName As String
Dim grbit As RenameColumnGrbitApi.JetRenameColumn(sesid, tableid, _
    name, newName, grbit)
```

``` csharp
public static void JetRenameColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string name,
    string newName,
    RenameColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="eb19c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb19c-108">Parameters</span></span>

  - <span data-ttu-id="eb19c-109">sesid</span><span class="sxs-lookup"><span data-stu-id="eb19c-109">sesid</span></span>  
    <span data-ttu-id="eb19c-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="eb19c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="eb19c-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="eb19c-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb19c-112">TableID</span><span class="sxs-lookup"><span data-stu-id="eb19c-112">tableid</span></span>  
    <span data-ttu-id="eb19c-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="eb19c-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="eb19c-114">A tabela que contém a coluna.</span><span class="sxs-lookup"><span data-stu-id="eb19c-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb19c-115">name</span><span class="sxs-lookup"><span data-stu-id="eb19c-115">name</span></span>  
    <span data-ttu-id="eb19c-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="eb19c-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="eb19c-117">O nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="eb19c-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb19c-118">newName</span><span class="sxs-lookup"><span data-stu-id="eb19c-118">newName</span></span>  
    <span data-ttu-id="eb19c-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="eb19c-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="eb19c-120">O novo nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="eb19c-120">The new name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb19c-121">grbit</span><span class="sxs-lookup"><span data-stu-id="eb19c-121">grbit</span></span>  
    <span data-ttu-id="eb19c-122">Tipo: [Microsoft. ISAM. ESENT. Interop. RenameColumnGrbit](./renamecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="eb19c-122">Type: [Microsoft.Isam.Esent.Interop.RenameColumnGrbit](./renamecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="eb19c-123">Opções de renomeação de coluna.</span><span class="sxs-lookup"><span data-stu-id="eb19c-123">Column rename options.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb19c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb19c-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb19c-125">Referência</span><span class="sxs-lookup"><span data-stu-id="eb19c-125">Reference</span></span>

[<span data-ttu-id="eb19c-126">Classe de API</span><span class="sxs-lookup"><span data-stu-id="eb19c-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="eb19c-127">Membros da API</span><span class="sxs-lookup"><span data-stu-id="eb19c-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="eb19c-128">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="eb19c-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
