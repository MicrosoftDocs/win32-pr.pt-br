---
description: 'Saiba mais sobre: método API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String JET_COLUMNDEF)'
title: Método API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String JET_COLUMNDEF)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100708
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4af99e7cfdc9f2f1fe83095ad92797ce0b34bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090148"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columndef"></a><span data-ttu-id="6be76-103">Método API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="6be76-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</span></span>

<span data-ttu-id="6be76-104">Recupera informações sobre uma coluna de tabela.</span><span class="sxs-lookup"><span data-stu-id="6be76-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="6be76-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6be76-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6be76-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6be76-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6be76-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6be76-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columndef)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="6be76-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6be76-108">Parameters</span></span>

  - <span data-ttu-id="6be76-109">sesid</span><span class="sxs-lookup"><span data-stu-id="6be76-109">sesid</span></span>  
    <span data-ttu-id="6be76-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6be76-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6be76-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6be76-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6be76-112">dbid</span><span class="sxs-lookup"><span data-stu-id="6be76-112">dbid</span></span>  
    <span data-ttu-id="6be76-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6be76-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="6be76-114">O banco de dados que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="6be76-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="6be76-115">tablename</span><span class="sxs-lookup"><span data-stu-id="6be76-115">tablename</span></span>  
    <span data-ttu-id="6be76-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6be76-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6be76-117">O nome da tabela que contém a coluna.</span><span class="sxs-lookup"><span data-stu-id="6be76-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="6be76-118">columnName</span><span class="sxs-lookup"><span data-stu-id="6be76-118">columnName</span></span>  
    <span data-ttu-id="6be76-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6be76-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6be76-120">O nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="6be76-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="6be76-121">columndef</span><span class="sxs-lookup"><span data-stu-id="6be76-121">columndef</span></span>  
    <span data-ttu-id="6be76-122">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="6be76-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="6be76-123">Preenchido com informações sobre a coluna.</span><span class="sxs-lookup"><span data-stu-id="6be76-123">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="6be76-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6be76-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6be76-125">Referência</span><span class="sxs-lookup"><span data-stu-id="6be76-125">Reference</span></span>

[<span data-ttu-id="6be76-126">Classe de API</span><span class="sxs-lookup"><span data-stu-id="6be76-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6be76-127">Membros da API</span><span class="sxs-lookup"><span data-stu-id="6be76-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6be76-128">Sobrecarga de JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="6be76-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="6be76-129">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6be76-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
