---
description: 'Saiba mais sobre: método API. JetEndExternalBackupInstance2'
title: Método API. JetEndExternalBackupInstance2
TOCTitle: 'JetEndExternalBackupInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance2(v=EXCHG.10)
ms:contentKeyID: 55100692
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71a405c5e0ba3a398071cc317e0d42dd98c4953d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164382"
---
# <a name="apijetendexternalbackupinstance2-method"></a><span data-ttu-id="ce38e-103">Método API. JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="ce38e-103">Api.JetEndExternalBackupInstance2 method</span></span>

<span data-ttu-id="ce38e-104">Encerra uma sessão de backup externo.</span><span class="sxs-lookup"><span data-stu-id="ce38e-104">Ends an external backup session.</span></span> <span data-ttu-id="ce38e-105">Essa API é a última API em uma série de APIs que devem ser chamadas para executar um backup online (não baseado em VSS) com êxito.</span><span class="sxs-lookup"><span data-stu-id="ce38e-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="ce38e-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ce38e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ce38e-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ce38e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ce38e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce38e-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As EndExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As EndExternalBackupGrbitApi.JetEndExternalBackupInstance2(instance, _
    grbit)
```

``` csharp
public static void JetEndExternalBackupInstance2(
    JET_INSTANCE instance,
    EndExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ce38e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce38e-109">Parameters</span></span>

  - <span data-ttu-id="ce38e-110">instance</span><span class="sxs-lookup"><span data-stu-id="ce38e-110">instance</span></span>  
    <span data-ttu-id="ce38e-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ce38e-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="ce38e-112">A instância para a qual terminar o backup.</span><span class="sxs-lookup"><span data-stu-id="ce38e-112">The instance to end the backup for.</span></span>

<!-- end list -->

  - <span data-ttu-id="ce38e-113">grbit</span><span class="sxs-lookup"><span data-stu-id="ce38e-113">grbit</span></span>  
    <span data-ttu-id="ce38e-114">Tipo: [Microsoft. ISAM. ESENT. Interop. EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ce38e-114">Type: [Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ce38e-115">Opções que especificam como o backup foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="ce38e-115">Options that specify how the backup ended.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce38e-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce38e-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ce38e-117">Referência</span><span class="sxs-lookup"><span data-stu-id="ce38e-117">Reference</span></span>

[<span data-ttu-id="ce38e-118">Classe de API</span><span class="sxs-lookup"><span data-stu-id="ce38e-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ce38e-119">Membros da API</span><span class="sxs-lookup"><span data-stu-id="ce38e-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ce38e-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ce38e-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
