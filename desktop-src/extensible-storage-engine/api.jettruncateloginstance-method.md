---
description: 'Saiba mais sobre: método API. JetTruncateLogInstance'
title: Método API. JetTruncateLogInstance
TOCTitle: 'JetTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jettruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55100815
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc1693b3f84cd594bfeca81a8e854e49e28d955f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922769"
---
# <a name="apijettruncateloginstance-method"></a><span data-ttu-id="477e2-103">Método API. JetTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="477e2-103">Api.JetTruncateLogInstance method</span></span>

<span data-ttu-id="477e2-104">Usado durante um backup iniciado pelo JetBeginExternalBackup para excluir qualquer arquivo de log de transações que não será mais necessário depois que o backup atual for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="477e2-104">Used during a backup initiated by JetBeginExternalBackup to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="477e2-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="477e2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="477e2-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="477e2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="477e2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="477e2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTruncateLogInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetTruncateLogInstance(instance)
```

``` csharp
public static void JetTruncateLogInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="477e2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="477e2-108">Parameters</span></span>

  - <span data-ttu-id="477e2-109">instance</span><span class="sxs-lookup"><span data-stu-id="477e2-109">instance</span></span>  
    <span data-ttu-id="477e2-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="477e2-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="477e2-111">A instância a ser truncada.</span><span class="sxs-lookup"><span data-stu-id="477e2-111">The instance to truncate.</span></span>

## <a name="see-also"></a><span data-ttu-id="477e2-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="477e2-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="477e2-113">Referência</span><span class="sxs-lookup"><span data-stu-id="477e2-113">Reference</span></span>

[<span data-ttu-id="477e2-114">Classe de API</span><span class="sxs-lookup"><span data-stu-id="477e2-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="477e2-115">Membros da API</span><span class="sxs-lookup"><span data-stu-id="477e2-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="477e2-116">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="477e2-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
