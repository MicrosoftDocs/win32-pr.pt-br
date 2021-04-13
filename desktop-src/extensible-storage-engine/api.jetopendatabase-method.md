---
description: 'Saiba mais sobre: método API. JetOpenDatabase'
title: Método API. JetOpenDatabase
TOCTitle: 'JetOpenDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopendatabase(v=EXCHG.10)
ms:contentKeyID: 55100768
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: faaff0eec2b5bc8a2c2f2a72a61f9f6a23f7d972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171773"
---
# <a name="apijetopendatabase-method"></a><span data-ttu-id="5390f-103">Método API. JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="5390f-103">Api.JetOpenDatabase method</span></span>

<span data-ttu-id="5390f-104">Abre um banco de dados anexado anteriormente com [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md)para uso com uma sessão de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5390f-104">Opens a database previously attached with [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md), for use with a database session.</span></span> <span data-ttu-id="5390f-105">Essa função pode ser chamada várias vezes para o mesmo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5390f-105">This function can be called multiple times for the same database.</span></span>

<span data-ttu-id="5390f-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5390f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5390f-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5390f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5390f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5390f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetOpenDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As OpenDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As OpenDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetOpenDatabase(sesid, _
    database, connect, dbid, grbit)
```

``` csharp
public static JET_wrn JetOpenDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    OpenDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5390f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5390f-109">Parameters</span></span>

  - <span data-ttu-id="5390f-110">sesid</span><span class="sxs-lookup"><span data-stu-id="5390f-110">sesid</span></span>  
    <span data-ttu-id="5390f-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5390f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5390f-112">A sessão que está abrindo o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5390f-112">The session that is opening the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="5390f-113">Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="5390f-113">database</span></span>  
    <span data-ttu-id="5390f-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5390f-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5390f-115">O banco de dados a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="5390f-115">The database to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="5390f-116">conectar</span><span class="sxs-lookup"><span data-stu-id="5390f-116">connect</span></span>  
    <span data-ttu-id="5390f-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5390f-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5390f-118">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5390f-118">Reserved for future use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5390f-119">dbid</span><span class="sxs-lookup"><span data-stu-id="5390f-119">dbid</span></span>  
    <span data-ttu-id="5390f-120">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5390f-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="5390f-121">Retorna a DBID do banco de dados anexado.</span><span class="sxs-lookup"><span data-stu-id="5390f-121">Returns the dbid of the attached database.</span></span>

<!-- end list -->

  - <span data-ttu-id="5390f-122">grbit</span><span class="sxs-lookup"><span data-stu-id="5390f-122">grbit</span></span>  
    <span data-ttu-id="5390f-123">Tipo: [Microsoft. ISAM. ESENT. Interop. OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5390f-123">Type: [Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5390f-124">Abra opções de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5390f-124">Open database options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5390f-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5390f-125">Return value</span></span>

<span data-ttu-id="5390f-126">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5390f-126">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="5390f-127">Um código de aviso de ESENT.</span><span class="sxs-lookup"><span data-stu-id="5390f-127">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5390f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5390f-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5390f-129">Referência</span><span class="sxs-lookup"><span data-stu-id="5390f-129">Reference</span></span>

[<span data-ttu-id="5390f-130">Classe de API</span><span class="sxs-lookup"><span data-stu-id="5390f-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5390f-131">Membros da API</span><span class="sxs-lookup"><span data-stu-id="5390f-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5390f-132">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5390f-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
