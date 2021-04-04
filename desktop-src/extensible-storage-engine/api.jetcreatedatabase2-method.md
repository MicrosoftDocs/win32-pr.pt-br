---
description: 'Saiba mais sobre: método API. JetCreateDatabase2'
title: Método API. JetCreateDatabase2
TOCTitle: 'JetCreateDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase2(v=EXCHG.10)
ms:contentKeyID: 55100671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8293a7c98451b0fd8bc46fbc13dde6b477a0ad09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646649"
---
# <a name="apijetcreatedatabase2-method"></a><span data-ttu-id="bc6d8-103">Método API. JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="bc6d8-103">Api.JetCreateDatabase2 method</span></span>

<span data-ttu-id="bc6d8-104">Cria e anexa um arquivo de banco de dados com um tamanho máximo de banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-104">Creates and attaches a database file with a maximum database size specified.</span></span>

<span data-ttu-id="bc6d8-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bc6d8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bc6d8-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bc6d8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bc6d8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc6d8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase2(sesid, database, _
    maxPages, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="bc6d8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc6d8-108">Parameters</span></span>

  - <span data-ttu-id="bc6d8-109">sesid</span><span class="sxs-lookup"><span data-stu-id="bc6d8-109">sesid</span></span>  
    <span data-ttu-id="bc6d8-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bc6d8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bc6d8-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc6d8-112">Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="bc6d8-112">database</span></span>  
    <span data-ttu-id="bc6d8-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="bc6d8-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="bc6d8-114">O caminho para o arquivo de banco de dados a ser criado.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc6d8-115">maxPages</span><span class="sxs-lookup"><span data-stu-id="bc6d8-115">maxPages</span></span>  
    <span data-ttu-id="bc6d8-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bc6d8-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="bc6d8-117">O tamanho máximo, em páginas de banco de dados, do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-117">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="bc6d8-118">Passar 0 significa que não há um máximo imposto.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-118">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc6d8-119">dbid</span><span class="sxs-lookup"><span data-stu-id="bc6d8-119">dbid</span></span>  
    <span data-ttu-id="bc6d8-120">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bc6d8-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="bc6d8-121">Retorna o DBID do novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-121">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc6d8-122">grbit</span><span class="sxs-lookup"><span data-stu-id="bc6d8-122">grbit</span></span>  
    <span data-ttu-id="bc6d8-123">Tipo: [Microsoft. ISAM. ESENT. Interop. CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bc6d8-123">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="bc6d8-124">Opções de criação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-124">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc6d8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc6d8-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bc6d8-126">Referência</span><span class="sxs-lookup"><span data-stu-id="bc6d8-126">Reference</span></span>

[<span data-ttu-id="bc6d8-127">Classe de API</span><span class="sxs-lookup"><span data-stu-id="bc6d8-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bc6d8-128">Membros da API</span><span class="sxs-lookup"><span data-stu-id="bc6d8-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bc6d8-129">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bc6d8-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
