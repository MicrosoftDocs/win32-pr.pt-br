---
description: 'Saiba mais sobre: método API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String JET_INDEXLIST)'
title: Método API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String JET_INDEXLIST)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100770
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2320b72a90ff97326c027b00cfeb5bf38453f68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758499"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist"></a><span data-ttu-id="a2a40-103">Método API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String JET_INDEXLIST)</span><span class="sxs-lookup"><span data-stu-id="a2a40-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="a2a40-104">**Observação: essa API agora está obsoleta.**</span><span class="sxs-lookup"><span data-stu-id="a2a40-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="a2a40-105">Recupera informações sobre índices em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="a2a40-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="a2a40-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a2a40-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a2a40-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a2a40-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a2a40-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2a40-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    ignored As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim ignored As String
Dim indexlist As JET_INDEXLISTApi.JetGetIndexInfo(sesid, dbid, _
    tablename, ignored, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string ignored,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="a2a40-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2a40-109">Parameters</span></span>

  - <span data-ttu-id="a2a40-110">sesid</span><span class="sxs-lookup"><span data-stu-id="a2a40-110">sesid</span></span>  
    <span data-ttu-id="a2a40-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a2a40-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a2a40-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a2a40-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a2a40-113">dbid</span><span class="sxs-lookup"><span data-stu-id="a2a40-113">dbid</span></span>  
    <span data-ttu-id="a2a40-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a2a40-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="a2a40-115">O banco de dados a ser usado.</span><span class="sxs-lookup"><span data-stu-id="a2a40-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a2a40-116">tablename</span><span class="sxs-lookup"><span data-stu-id="a2a40-116">tablename</span></span>  
    <span data-ttu-id="a2a40-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a2a40-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a2a40-118">O nome da tabela sobre a qual recuperar informações de índice.</span><span class="sxs-lookup"><span data-stu-id="a2a40-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="a2a40-119">ignorado</span><span class="sxs-lookup"><span data-stu-id="a2a40-119">ignored</span></span>  
    <span data-ttu-id="a2a40-120">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a2a40-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a2a40-121">Este parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="a2a40-121">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="a2a40-122">IndexList</span><span class="sxs-lookup"><span data-stu-id="a2a40-122">indexlist</span></span>  
    <span data-ttu-id="a2a40-123">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="a2a40-123">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="a2a40-124">Preenchido com informações sobre índices na tabela.</span><span class="sxs-lookup"><span data-stu-id="a2a40-124">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2a40-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2a40-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a2a40-126">Referência</span><span class="sxs-lookup"><span data-stu-id="a2a40-126">Reference</span></span>

[<span data-ttu-id="a2a40-127">Classe de API</span><span class="sxs-lookup"><span data-stu-id="a2a40-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a2a40-128">Membros da API</span><span class="sxs-lookup"><span data-stu-id="a2a40-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a2a40-129">Sobrecarga de JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="a2a40-129">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="a2a40-130">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a2a40-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
