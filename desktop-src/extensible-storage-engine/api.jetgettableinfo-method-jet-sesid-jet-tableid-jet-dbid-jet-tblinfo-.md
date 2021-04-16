---
description: 'Saiba mais sobre: método API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)'
title: Método API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100736
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e955a1b854162bd8eca4e19506329c2cf6016e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765081"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-jet_dbid-jet_tblinfo"></a><span data-ttu-id="7b5df-103">Método API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID JET_TblInfo)</span><span class="sxs-lookup"><span data-stu-id="7b5df-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</span></span>

<span data-ttu-id="7b5df-104">Recupera várias partes de informações sobre uma tabela em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7b5df-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="7b5df-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7b5df-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7b5df-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7b5df-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7b5df-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b5df-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As JET_DBID, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As JET_DBID
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_DBID result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="7b5df-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b5df-108">Parameters</span></span>

  - <span data-ttu-id="7b5df-109">sesid</span><span class="sxs-lookup"><span data-stu-id="7b5df-109">sesid</span></span>  
    <span data-ttu-id="7b5df-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b5df-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7b5df-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7b5df-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b5df-112">TableID</span><span class="sxs-lookup"><span data-stu-id="7b5df-112">tableid</span></span>  
    <span data-ttu-id="7b5df-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b5df-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7b5df-114">A tabela da qual recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="7b5df-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b5df-115">result</span><span class="sxs-lookup"><span data-stu-id="7b5df-115">result</span></span>  
    <span data-ttu-id="7b5df-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b5df-116">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="7b5df-117">Informações recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7b5df-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b5df-118">infoLevel</span><span class="sxs-lookup"><span data-stu-id="7b5df-118">infoLevel</span></span>  
    <span data-ttu-id="7b5df-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7b5df-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="7b5df-120">O tipo de informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7b5df-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5df-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b5df-121">Remarks</span></span>

<span data-ttu-id="7b5df-122">Essa sobrecarga é usada com [DBID](./jet-tblinfo-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="7b5df-122">This overload is used with [Dbid](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7b5df-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b5df-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7b5df-124">Referência</span><span class="sxs-lookup"><span data-stu-id="7b5df-124">Reference</span></span>

[<span data-ttu-id="7b5df-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="7b5df-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7b5df-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="7b5df-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7b5df-127">Sobrecarga de JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="7b5df-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="7b5df-128">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7b5df-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
