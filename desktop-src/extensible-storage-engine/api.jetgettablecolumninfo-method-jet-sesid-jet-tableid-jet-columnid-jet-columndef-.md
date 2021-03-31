---
description: 'Saiba mais sobre: método API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)'
title: Método API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID JET_COLUMNDEF)
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100730
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa120cf78001ed608a2385e07f388ae91bc9b425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662984"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-jet_columnid-jet_columndef"></a><span data-ttu-id="a9ac0-103">Método API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="a9ac0-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</span></span>

<span data-ttu-id="a9ac0-104">Recupera informações sobre uma coluna de tabela.</span><span class="sxs-lookup"><span data-stu-id="a9ac0-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="a9ac0-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a9ac0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a9ac0-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a9ac0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ac0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9ac0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim columndef As JET_COLUMNDEFApi.JetGetTableColumnInfo(sesid, _
    tableid, columnid, columndef)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="a9ac0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9ac0-108">Parameters</span></span>

  - <span data-ttu-id="a9ac0-109">sesid</span><span class="sxs-lookup"><span data-stu-id="a9ac0-109">sesid</span></span>  
    <span data-ttu-id="a9ac0-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a9ac0-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a9ac0-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a9ac0-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9ac0-112">TableID</span><span class="sxs-lookup"><span data-stu-id="a9ac0-112">tableid</span></span>  
    <span data-ttu-id="a9ac0-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a9ac0-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a9ac0-114">A tabela que contém a coluna.</span><span class="sxs-lookup"><span data-stu-id="a9ac0-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9ac0-115">columnid</span><span class="sxs-lookup"><span data-stu-id="a9ac0-115">columnid</span></span>  
    <span data-ttu-id="a9ac0-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a9ac0-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="a9ac0-117">O columnid da coluna.</span><span class="sxs-lookup"><span data-stu-id="a9ac0-117">The columnid of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9ac0-118">columndef</span><span class="sxs-lookup"><span data-stu-id="a9ac0-118">columndef</span></span>  
    <span data-ttu-id="a9ac0-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="a9ac0-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="a9ac0-120">Preenchido com informações sobre a coluna.</span><span class="sxs-lookup"><span data-stu-id="a9ac0-120">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9ac0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9ac0-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a9ac0-122">Referência</span><span class="sxs-lookup"><span data-stu-id="a9ac0-122">Reference</span></span>

[<span data-ttu-id="a9ac0-123">Classe de API</span><span class="sxs-lookup"><span data-stu-id="a9ac0-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a9ac0-124">Membros da API</span><span class="sxs-lookup"><span data-stu-id="a9ac0-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a9ac0-125">Sobrecarga de JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="a9ac0-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="a9ac0-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a9ac0-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
