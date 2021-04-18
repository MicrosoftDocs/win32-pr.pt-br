---
description: 'Saiba mais sobre: método VistaApi. JetGetRecordSize'
title: Método VistaApi. JetGetRecordSize (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'JetGetRecordSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE@,Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetrecordsize(v=EXCHG.10)
ms:contentKeyID: 55104285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37576e39d83270dcac3333e4d1f78fce32bb2669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811456"
---
# <a name="vistaapijetgetrecordsize-method"></a><span data-ttu-id="3aec3-103">Método VistaApi. JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="3aec3-103">VistaApi.JetGetRecordSize method</span></span>

<span data-ttu-id="3aec3-104">Recupera informações de tamanho de registro do local desejado.</span><span class="sxs-lookup"><span data-stu-id="3aec3-104">Retrieves record size information from the desired location.</span></span>

<span data-ttu-id="3aec3-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3aec3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="3aec3-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3aec3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3aec3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3aec3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetRecordSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ByRef recsize As JET_RECSIZE, _
    grbit As GetRecordSizeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recsize As JET_RECSIZE
Dim grbit As GetRecordSizeGrbitVistaApi.JetGetRecordSize(sesid, tableid, _
    recsize, grbit)
```

``` csharp
public static void JetGetRecordSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ref JET_RECSIZE recsize,
    GetRecordSizeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3aec3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3aec3-108">Parameters</span></span>

  - <span data-ttu-id="3aec3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="3aec3-109">sesid</span></span>  
    <span data-ttu-id="3aec3-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3aec3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3aec3-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="3aec3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3aec3-112">TableID</span><span class="sxs-lookup"><span data-stu-id="3aec3-112">tableid</span></span>  
    <span data-ttu-id="3aec3-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3aec3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3aec3-114">O cursor que será usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="3aec3-114">The cursor that will be used for the API call.</span></span> <span data-ttu-id="3aec3-115">O cursor deve ser posicionado em um registro ou ter uma atualização preparada.</span><span class="sxs-lookup"><span data-stu-id="3aec3-115">The cursor must be positioned on a record, or have an update prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="3aec3-116">recsize</span><span class="sxs-lookup"><span data-stu-id="3aec3-116">recsize</span></span>  
    <span data-ttu-id="3aec3-117">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="3aec3-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="3aec3-118">Retorna o tamanho do registro.</span><span class="sxs-lookup"><span data-stu-id="3aec3-118">Returns the size of the record.</span></span>

<!-- end list -->

  - <span data-ttu-id="3aec3-119">grbit</span><span class="sxs-lookup"><span data-stu-id="3aec3-119">grbit</span></span>  
    <span data-ttu-id="3aec3-120">Tipo: [Microsoft. ISAM. ESENT. Interop. GetRecordSizeGrbit](./getrecordsizegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3aec3-120">Type: [Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit](./getrecordsizegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3aec3-121">Opções de chamada.</span><span class="sxs-lookup"><span data-stu-id="3aec3-121">Call options.</span></span>

## <a name="see-also"></a><span data-ttu-id="3aec3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3aec3-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3aec3-123">Referência</span><span class="sxs-lookup"><span data-stu-id="3aec3-123">Reference</span></span>

[<span data-ttu-id="3aec3-124">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="3aec3-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="3aec3-125">Membros do VistaApi</span><span class="sxs-lookup"><span data-stu-id="3aec3-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="3aec3-126">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="3aec3-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
