---
description: 'Saiba mais sobre: método API. JetBackupInstance'
title: Método API. JetBackupInstance
TOCTitle: 'JetBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.BackupGrbit,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55107221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73c5b44f1f0b69aaed6066635ad4e82690bc3c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089825"
---
# <a name="apijetbackupinstance-method"></a><span data-ttu-id="719ea-103">Método API. JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="719ea-103">Api.JetBackupInstance method</span></span>

<span data-ttu-id="719ea-104">Executa um backup de streaming de uma instância do, incluindo todos os bancos de dados anexados, em um diretório.</span><span class="sxs-lookup"><span data-stu-id="719ea-104">Performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="719ea-105">Com vários métodos de backup com suporte no mecanismo, essa é a função mais simples e encapsulada.</span><span class="sxs-lookup"><span data-stu-id="719ea-105">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="719ea-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="719ea-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="719ea-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="719ea-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="719ea-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="719ea-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBackupInstance ( _
    instance As JET_INSTANCE, _
    destination As String, _
    grbit As BackupGrbit, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim destination As String
Dim grbit As BackupGrbit
Dim statusCallback As JET_PFNSTATUSApi.JetBackupInstance(instance, _
    destination, grbit, statusCallback)
```

``` csharp
public static void JetBackupInstance(
    JET_INSTANCE instance,
    string destination,
    BackupGrbit grbit,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="719ea-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="719ea-109">Parameters</span></span>

  - <span data-ttu-id="719ea-110">instance</span><span class="sxs-lookup"><span data-stu-id="719ea-110">instance</span></span>  
    <span data-ttu-id="719ea-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="719ea-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="719ea-112">A instância para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="719ea-112">The instance to backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="719ea-113">destino</span><span class="sxs-lookup"><span data-stu-id="719ea-113">destination</span></span>  
    <span data-ttu-id="719ea-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="719ea-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="719ea-115">O diretório em que o backup deve ser armazenado.</span><span class="sxs-lookup"><span data-stu-id="719ea-115">The directory where the backup is to be stored.</span></span> <span data-ttu-id="719ea-116">Se o caminho de backup for nulo para usar a função, o truncará os logs, se possível.</span><span class="sxs-lookup"><span data-stu-id="719ea-116">If the backup path is null to use the function will truncate the logs, if possible.</span></span>

<!-- end list -->

  - <span data-ttu-id="719ea-117">grbit</span><span class="sxs-lookup"><span data-stu-id="719ea-117">grbit</span></span>  
    <span data-ttu-id="719ea-118">Tipo: [Microsoft. ISAM. ESENT. Interop. BackupGrbit](./backupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="719ea-118">Type: [Microsoft.Isam.Esent.Interop.BackupGrbit](./backupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="719ea-119">Opções de backup.</span><span class="sxs-lookup"><span data-stu-id="719ea-119">Backup options.</span></span>

<!-- end list -->

  - <span data-ttu-id="719ea-120">statusCallback</span><span class="sxs-lookup"><span data-stu-id="719ea-120">statusCallback</span></span>  
    <span data-ttu-id="719ea-121">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="719ea-121">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="719ea-122">Retorno de chamada de notificação de status opcional.</span><span class="sxs-lookup"><span data-stu-id="719ea-122">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="719ea-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="719ea-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="719ea-124">Referência</span><span class="sxs-lookup"><span data-stu-id="719ea-124">Reference</span></span>

[<span data-ttu-id="719ea-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="719ea-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="719ea-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="719ea-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="719ea-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="719ea-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
