---
description: 'Saiba mais sobre: método API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String JET_COLUMNLIST)'
title: Método API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String JET_COLUMNLIST)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100703
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f3f0ea95e82217f0d9b44e6a00558d3530a7616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791495"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columnlist"></a><span data-ttu-id="24b05-103">Método API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String JET_COLUMNLIST)</span><span class="sxs-lookup"><span data-stu-id="24b05-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)</span></span>

<span data-ttu-id="24b05-104">Recupera informações sobre todas as colunas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="24b05-104">Retrieves information about all columns in a table.</span></span>

<span data-ttu-id="24b05-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="24b05-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="24b05-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="24b05-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="24b05-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24b05-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columnlist As JET_COLUMNLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columnlist As JET_COLUMNLISTApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columnlist)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNLIST columnlist
)
```

#### <a name="parameters"></a><span data-ttu-id="24b05-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24b05-108">Parameters</span></span>

  - <span data-ttu-id="24b05-109">sesid</span><span class="sxs-lookup"><span data-stu-id="24b05-109">sesid</span></span>  
    <span data-ttu-id="24b05-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24b05-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="24b05-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="24b05-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="24b05-112">dbid</span><span class="sxs-lookup"><span data-stu-id="24b05-112">dbid</span></span>  
    <span data-ttu-id="24b05-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24b05-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="24b05-114">O banco de dados que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="24b05-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="24b05-115">tablename</span><span class="sxs-lookup"><span data-stu-id="24b05-115">tablename</span></span>  
    <span data-ttu-id="24b05-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="24b05-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="24b05-117">O nome da tabela que contém a coluna.</span><span class="sxs-lookup"><span data-stu-id="24b05-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="24b05-118">columnName</span><span class="sxs-lookup"><span data-stu-id="24b05-118">columnName</span></span>  
    <span data-ttu-id="24b05-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="24b05-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="24b05-120">Este parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="24b05-120">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="24b05-121">colunalist</span><span class="sxs-lookup"><span data-stu-id="24b05-121">columnlist</span></span>  
    <span data-ttu-id="24b05-122">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="24b05-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span></span>  
    
    <span data-ttu-id="24b05-123">Preenchido com informações sobre as colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="24b05-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="24b05-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="24b05-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="24b05-125">Referência</span><span class="sxs-lookup"><span data-stu-id="24b05-125">Reference</span></span>

[<span data-ttu-id="24b05-126">Classe de API</span><span class="sxs-lookup"><span data-stu-id="24b05-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="24b05-127">Membros da API</span><span class="sxs-lookup"><span data-stu-id="24b05-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="24b05-128">Sobrecarga de JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="24b05-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="24b05-129">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="24b05-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
