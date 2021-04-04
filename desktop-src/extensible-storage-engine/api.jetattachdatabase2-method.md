---
description: 'Saiba mais sobre: método API. JetAttachDatabase2'
title: Método API. JetAttachDatabase2
TOCTitle: 'JetAttachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55107224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 33d91f0746b3ebf178bd61de58919ab99d85b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646967"
---
# <a name="apijetattachdatabase2-method"></a><span data-ttu-id="f6dd0-103">Método API. JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="f6dd0-103">Api.JetAttachDatabase2 method</span></span>

<span data-ttu-id="f6dd0-104">Anexa um arquivo de banco de dados para uso com uma instância de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-104">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="f6dd0-105">Para usar o banco de dados, será necessário abri-lo subsequentemente com [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="f6dd0-105">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="f6dd0-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f6dd0-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6dd0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6dd0-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetAttachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase2(sesid, _
    database, maxPages, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f6dd0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6dd0-109">Parameters</span></span>

  - <span data-ttu-id="f6dd0-110">sesid</span><span class="sxs-lookup"><span data-stu-id="f6dd0-110">sesid</span></span>  
    <span data-ttu-id="f6dd0-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f6dd0-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f6dd0-113">Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="f6dd0-113">database</span></span>  
    <span data-ttu-id="f6dd0-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f6dd0-115">O banco de dados a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-115">The database to attach.</span></span>

<!-- end list -->

  - <span data-ttu-id="f6dd0-116">maxPages</span><span class="sxs-lookup"><span data-stu-id="f6dd0-116">maxPages</span></span>  
    <span data-ttu-id="f6dd0-117">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f6dd0-118">O tamanho máximo, em páginas de banco de dados, do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-118">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="f6dd0-119">Passar 0 significa que não há um máximo imposto.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-119">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="f6dd0-120">grbit</span><span class="sxs-lookup"><span data-stu-id="f6dd0-120">grbit</span></span>  
    <span data-ttu-id="f6dd0-121">Tipo: [Microsoft. ISAM. ESENT. Interop. AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-121">Type: [Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f6dd0-122">Opções de anexação.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-122">Attach options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f6dd0-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6dd0-123">Return value</span></span>

<span data-ttu-id="f6dd0-124">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f6dd0-124">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="f6dd0-125">Um código de aviso de ESENT.</span><span class="sxs-lookup"><span data-stu-id="f6dd0-125">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6dd0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6dd0-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6dd0-127">Referência</span><span class="sxs-lookup"><span data-stu-id="f6dd0-127">Reference</span></span>

[<span data-ttu-id="f6dd0-128">Classe de API</span><span class="sxs-lookup"><span data-stu-id="f6dd0-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f6dd0-129">Membros da API</span><span class="sxs-lookup"><span data-stu-id="f6dd0-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f6dd0-130">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f6dd0-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
