---
description: 'Saiba mais sobre: método API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, String JET_COLUMNDEF)'
title: Método API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, String JET_COLUMNDEF)
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100724
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60e984fdb1577dc69a352c327c1af605e0d441d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296499"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-string-jet_columndef"></a><span data-ttu-id="cd8f8-103">Método API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, String JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="cd8f8-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)</span></span>

<span data-ttu-id="cd8f8-104">Recupera informações sobre uma coluna de tabela.</span><span class="sxs-lookup"><span data-stu-id="cd8f8-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="cd8f8-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cd8f8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cd8f8-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cd8f8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cd8f8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd8f8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetTableColumnInfo(sesid, _
    tableid, columnName, columndef)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="cd8f8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd8f8-108">Parameters</span></span>

  - <span data-ttu-id="cd8f8-109">sesid</span><span class="sxs-lookup"><span data-stu-id="cd8f8-109">sesid</span></span>  
    <span data-ttu-id="cd8f8-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cd8f8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cd8f8-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="cd8f8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cd8f8-112">TableID</span><span class="sxs-lookup"><span data-stu-id="cd8f8-112">tableid</span></span>  
    <span data-ttu-id="cd8f8-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cd8f8-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="cd8f8-114">A tabela que contém a coluna.</span><span class="sxs-lookup"><span data-stu-id="cd8f8-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="cd8f8-115">columnName</span><span class="sxs-lookup"><span data-stu-id="cd8f8-115">columnName</span></span>  
    <span data-ttu-id="cd8f8-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="cd8f8-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="cd8f8-117">O nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="cd8f8-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="cd8f8-118">columndef</span><span class="sxs-lookup"><span data-stu-id="cd8f8-118">columndef</span></span>  
    <span data-ttu-id="cd8f8-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="cd8f8-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="cd8f8-120">Preenchido com informações sobre a coluna.</span><span class="sxs-lookup"><span data-stu-id="cd8f8-120">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd8f8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd8f8-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cd8f8-122">Referência</span><span class="sxs-lookup"><span data-stu-id="cd8f8-122">Reference</span></span>

[<span data-ttu-id="cd8f8-123">Classe de API</span><span class="sxs-lookup"><span data-stu-id="cd8f8-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cd8f8-124">Membros da API</span><span class="sxs-lookup"><span data-stu-id="cd8f8-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cd8f8-125">Sobrecarga de JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="cd8f8-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="cd8f8-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cd8f8-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
