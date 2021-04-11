---
description: 'Saiba mais sobre: método API. JetResetTableSequential'
title: Método API. JetResetTableSequential
TOCTitle: 'JetResetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b45ca118894015df7cda56201733cdaad9b88d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171762"
---
# <a name="apijetresettablesequential-method"></a><span data-ttu-id="bb1cb-103">Método API. JetResetTableSequential</span><span class="sxs-lookup"><span data-stu-id="bb1cb-103">Api.JetResetTableSequential method</span></span>

<span data-ttu-id="bb1cb-104">Notifica o mecanismo de banco de dados de que o aplicativo não está mais verificando o índice inteiro no qual o cursor está posicionado.</span><span class="sxs-lookup"><span data-stu-id="bb1cb-104">Notifies the database engine that the application is no longer scanning the entire index the cursor is positioned on.</span></span> <span data-ttu-id="bb1cb-105">Essa chamada reverte uma notificação enviada por [JetSetTableSequential (JET_SESID, JET_TABLEID, SetTableSequentialGrbit)](./api.jetsettablesequential-method.md).</span><span class="sxs-lookup"><span data-stu-id="bb1cb-105">This call reverses a notification sent by [JetSetTableSequential(JET_SESID, JET_TABLEID, SetTableSequentialGrbit)](./api.jetsettablesequential-method.md).</span></span>

<span data-ttu-id="bb1cb-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bb1cb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bb1cb-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bb1cb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bb1cb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb1cb-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As ResetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As ResetTableSequentialGrbitApi.JetResetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetResetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ResetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="bb1cb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb1cb-109">Parameters</span></span>

  - <span data-ttu-id="bb1cb-110">sesid</span><span class="sxs-lookup"><span data-stu-id="bb1cb-110">sesid</span></span>  
    <span data-ttu-id="bb1cb-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bb1cb-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bb1cb-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="bb1cb-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="bb1cb-113">TableID</span><span class="sxs-lookup"><span data-stu-id="bb1cb-113">tableid</span></span>  
    <span data-ttu-id="bb1cb-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bb1cb-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bb1cb-115">O cursor que estava acessando os dados.</span><span class="sxs-lookup"><span data-stu-id="bb1cb-115">The cursor that was accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="bb1cb-116">grbit</span><span class="sxs-lookup"><span data-stu-id="bb1cb-116">grbit</span></span>  
    <span data-ttu-id="bb1cb-117">Tipo: [Microsoft. ISAM. ESENT. Interop. ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bb1cb-117">Type: [Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="bb1cb-118">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="bb1cb-118">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb1cb-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb1cb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bb1cb-120">Referência</span><span class="sxs-lookup"><span data-stu-id="bb1cb-120">Reference</span></span>

[<span data-ttu-id="bb1cb-121">Classe de API</span><span class="sxs-lookup"><span data-stu-id="bb1cb-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bb1cb-122">Membros da API</span><span class="sxs-lookup"><span data-stu-id="bb1cb-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bb1cb-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bb1cb-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
