---
description: 'Saiba mais sobre: método API. JetEndExternalBackupInstance'
title: Método API. JetEndExternalBackupInstance
TOCTitle: 'JetEndExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100691
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16ec4dc235f677ba42b4ae3bae10a79b9d494576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920789"
---
# <a name="apijetendexternalbackupinstance-method"></a><span data-ttu-id="42ad6-103">Método API. JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="42ad6-103">Api.JetEndExternalBackupInstance method</span></span>

<span data-ttu-id="42ad6-104">Encerra uma sessão de backup externo.</span><span class="sxs-lookup"><span data-stu-id="42ad6-104">Ends an external backup session.</span></span> <span data-ttu-id="42ad6-105">Essa API é a última API em uma série de APIs que devem ser chamadas para executar um backup online (não baseado em VSS) com êxito.</span><span class="sxs-lookup"><span data-stu-id="42ad6-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="42ad6-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="42ad6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="42ad6-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="42ad6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="42ad6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42ad6-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetEndExternalBackupInstance(instance)
```

``` csharp
public static void JetEndExternalBackupInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="42ad6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42ad6-109">Parameters</span></span>

  - <span data-ttu-id="42ad6-110">instance</span><span class="sxs-lookup"><span data-stu-id="42ad6-110">instance</span></span>  
    <span data-ttu-id="42ad6-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="42ad6-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="42ad6-112">A instância para a qual terminar o backup.</span><span class="sxs-lookup"><span data-stu-id="42ad6-112">The instance to end the backup for.</span></span>

## <a name="see-also"></a><span data-ttu-id="42ad6-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="42ad6-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="42ad6-114">Referência</span><span class="sxs-lookup"><span data-stu-id="42ad6-114">Reference</span></span>

[<span data-ttu-id="42ad6-115">Classe de API</span><span class="sxs-lookup"><span data-stu-id="42ad6-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="42ad6-116">Membros da API</span><span class="sxs-lookup"><span data-stu-id="42ad6-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="42ad6-117">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="42ad6-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
