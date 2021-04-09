---
description: 'Saiba mais sobre: método API. JetBeginExternalBackupInstance'
title: Método API. JetBeginExternalBackupInstance
TOCTitle: 'JetBeginExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbeginexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100659
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c42f5d1f62de0af7582247fb47d407f82981a42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920794"
---
# <a name="apijetbeginexternalbackupinstance-method"></a><span data-ttu-id="55fe4-103">Método API. JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="55fe4-103">Api.JetBeginExternalBackupInstance method</span></span>

<span data-ttu-id="55fe4-104">Inicia um backup externo enquanto o mecanismo e o banco de dados estão online e ativos.</span><span class="sxs-lookup"><span data-stu-id="55fe4-104">Initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="55fe4-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55fe4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="55fe4-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55fe4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55fe4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55fe4-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginExternalBackupInstance ( _
    instance As JET_INSTANCE, _
    grbit As BeginExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As BeginExternalBackupGrbitApi.JetBeginExternalBackupInstance(instance, _
    grbit)
```

``` csharp
public static void JetBeginExternalBackupInstance(
    JET_INSTANCE instance,
    BeginExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="55fe4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55fe4-108">Parameters</span></span>

  - <span data-ttu-id="55fe4-109">instance</span><span class="sxs-lookup"><span data-stu-id="55fe4-109">instance</span></span>  
    <span data-ttu-id="55fe4-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="55fe4-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="55fe4-111">A instância se prepara para o backup.</span><span class="sxs-lookup"><span data-stu-id="55fe4-111">The instance prepare for backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="55fe4-112">grbit</span><span class="sxs-lookup"><span data-stu-id="55fe4-112">grbit</span></span>  
    <span data-ttu-id="55fe4-113">Tipo: [Microsoft. ISAM. ESENT. Interop. BeginExternalBackupGrbit](./beginexternalbackupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="55fe4-113">Type: [Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit](./beginexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="55fe4-114">Opções de backup.</span><span class="sxs-lookup"><span data-stu-id="55fe4-114">Backup options.</span></span>

## <a name="see-also"></a><span data-ttu-id="55fe4-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="55fe4-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55fe4-116">Referência</span><span class="sxs-lookup"><span data-stu-id="55fe4-116">Reference</span></span>

[<span data-ttu-id="55fe4-117">Classe de API</span><span class="sxs-lookup"><span data-stu-id="55fe4-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="55fe4-118">Membros da API</span><span class="sxs-lookup"><span data-stu-id="55fe4-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="55fe4-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="55fe4-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
