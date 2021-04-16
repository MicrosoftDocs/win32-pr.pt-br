---
description: 'Saiba mais sobre: método API. JetCreateDatabase'
title: Método API. JetCreateDatabase
TOCTitle: 'JetCreateDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase(v=EXCHG.10)
ms:contentKeyID: 55100748
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe427c270baf8a6d05e5d0ae99e1dc393208da01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754290"
---
# <a name="apijetcreatedatabase-method"></a><span data-ttu-id="c8917-103">Método API. JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="c8917-103">Api.JetCreateDatabase method</span></span>

<span data-ttu-id="c8917-104">Cria e anexa um arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c8917-104">Creates and attaches a database file.</span></span>

<span data-ttu-id="c8917-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c8917-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c8917-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c8917-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c8917-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8917-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase(sesid, database, _
    connect, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c8917-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8917-108">Parameters</span></span>

  - <span data-ttu-id="c8917-109">sesid</span><span class="sxs-lookup"><span data-stu-id="c8917-109">sesid</span></span>  
    <span data-ttu-id="c8917-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c8917-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c8917-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c8917-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c8917-112">Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="c8917-112">database</span></span>  
    <span data-ttu-id="c8917-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c8917-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c8917-114">O caminho para o arquivo de banco de dados a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c8917-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="c8917-115">conectar</span><span class="sxs-lookup"><span data-stu-id="c8917-115">connect</span></span>  
    <span data-ttu-id="c8917-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c8917-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c8917-117">O parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="c8917-117">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="c8917-118">dbid</span><span class="sxs-lookup"><span data-stu-id="c8917-118">dbid</span></span>  
    <span data-ttu-id="c8917-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c8917-119">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="c8917-120">Retorna o DBID do novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c8917-120">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="c8917-121">grbit</span><span class="sxs-lookup"><span data-stu-id="c8917-121">grbit</span></span>  
    <span data-ttu-id="c8917-122">Tipo: [Microsoft. ISAM. ESENT. Interop. CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c8917-122">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c8917-123">Opções de criação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c8917-123">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8917-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8917-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c8917-125">Referência</span><span class="sxs-lookup"><span data-stu-id="c8917-125">Reference</span></span>

[<span data-ttu-id="c8917-126">Classe de API</span><span class="sxs-lookup"><span data-stu-id="c8917-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c8917-127">Membros da API</span><span class="sxs-lookup"><span data-stu-id="c8917-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c8917-128">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c8917-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
