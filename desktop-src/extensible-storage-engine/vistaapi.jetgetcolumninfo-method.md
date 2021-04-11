---
description: 'Saiba mais sobre: método VistaApi. JetGetColumnInfo'
title: Método VistaApi. JetGetColumnInfo (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'JetGetColumnInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55104283
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ae090fa5279b9ec60a3be88b4ebda393322b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090647"
---
# <a name="vistaapijetgetcolumninfo-method"></a><span data-ttu-id="2eb41-103">Método VistaApi. JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="2eb41-103">VistaApi.JetGetColumnInfo method</span></span>

<span data-ttu-id="2eb41-104">Recupera informações sobre uma coluna em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="2eb41-104">Retrieves information about a column in a table.</span></span>

<span data-ttu-id="2eb41-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2eb41-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="2eb41-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2eb41-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb41-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2eb41-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnid As JET_COLUMNID
Dim columnbase As JET_COLUMNBASEVistaApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnid, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    JET_COLUMNID columnid,
    out JET_COLUMNBASE columnbase
)
```

#### <a name="parameters"></a><span data-ttu-id="2eb41-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eb41-108">Parameters</span></span>

  - <span data-ttu-id="2eb41-109">sesid</span><span class="sxs-lookup"><span data-stu-id="2eb41-109">sesid</span></span>  
    <span data-ttu-id="2eb41-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2eb41-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2eb41-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="2eb41-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2eb41-112">dbid</span><span class="sxs-lookup"><span data-stu-id="2eb41-112">dbid</span></span>  
    <span data-ttu-id="2eb41-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2eb41-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="2eb41-114">O banco de dados que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="2eb41-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="2eb41-115">tablename</span><span class="sxs-lookup"><span data-stu-id="2eb41-115">tablename</span></span>  
    <span data-ttu-id="2eb41-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2eb41-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2eb41-117">O nome da tabela que contém a coluna.</span><span class="sxs-lookup"><span data-stu-id="2eb41-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="2eb41-118">columnid</span><span class="sxs-lookup"><span data-stu-id="2eb41-118">columnid</span></span>  
    <span data-ttu-id="2eb41-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2eb41-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="2eb41-120">A ID da coluna.</span><span class="sxs-lookup"><span data-stu-id="2eb41-120">The ID of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="2eb41-121">columnbase</span><span class="sxs-lookup"><span data-stu-id="2eb41-121">columnbase</span></span>  
    <span data-ttu-id="2eb41-122">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="2eb41-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="2eb41-123">Preenchido com informações sobre as colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="2eb41-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="2eb41-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2eb41-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2eb41-125">Referência</span><span class="sxs-lookup"><span data-stu-id="2eb41-125">Reference</span></span>

[<span data-ttu-id="2eb41-126">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="2eb41-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="2eb41-127">Membros do VistaApi</span><span class="sxs-lookup"><span data-stu-id="2eb41-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="2eb41-128">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="2eb41-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
