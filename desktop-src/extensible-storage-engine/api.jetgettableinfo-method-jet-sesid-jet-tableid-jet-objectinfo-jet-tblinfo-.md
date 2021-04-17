---
description: 'Saiba mais sobre: método API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)'
title: Método API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_OBJECTINFO@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100739
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
ms.openlocfilehash: fbc95c771e2610ec23bdf503cdefa0399ee219ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761705"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-jet_objectinfo-jet_tblinfo"></a><span data-ttu-id="e2967-103">Método API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO JET_TblInfo)</span><span class="sxs-lookup"><span data-stu-id="e2967-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</span></span>

<span data-ttu-id="e2967-104">Recupera várias partes de informações sobre uma tabela em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e2967-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="e2967-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2967-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2967-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2967-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2967-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2967-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As JET_OBJECTINFO, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As JET_OBJECTINFO
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_OBJECTINFO result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="e2967-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2967-108">Parameters</span></span>

  - <span data-ttu-id="e2967-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e2967-109">sesid</span></span>  
    <span data-ttu-id="e2967-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e2967-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e2967-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e2967-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2967-112">TableID</span><span class="sxs-lookup"><span data-stu-id="e2967-112">tableid</span></span>  
    <span data-ttu-id="e2967-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e2967-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e2967-114">A tabela da qual recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="e2967-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2967-115">result</span><span class="sxs-lookup"><span data-stu-id="e2967-115">result</span></span>  
    <span data-ttu-id="e2967-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="e2967-116">Type: [Microsoft.Isam.Esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span></span>  
    
    <span data-ttu-id="e2967-117">Informações recuperadas.</span><span class="sxs-lookup"><span data-stu-id="e2967-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2967-118">infoLevel</span><span class="sxs-lookup"><span data-stu-id="e2967-118">infoLevel</span></span>  
    <span data-ttu-id="e2967-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e2967-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="e2967-120">O tipo de informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="e2967-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2967-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2967-121">Remarks</span></span>

<span data-ttu-id="e2967-122">Essa sobrecarga é usada com o [padrão](./jet-tblinfo-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="e2967-122">This overload is used with [Default](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e2967-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2967-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2967-124">Referência</span><span class="sxs-lookup"><span data-stu-id="e2967-124">Reference</span></span>

[<span data-ttu-id="e2967-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="e2967-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e2967-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="e2967-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e2967-127">Sobrecarga de JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="e2967-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="e2967-128">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e2967-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
