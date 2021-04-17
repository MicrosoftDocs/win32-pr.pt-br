---
description: 'Saiba mais sobre: método API. JetRestoreInstance'
title: Método API. JetRestoreInstance
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789614"
---
# <a name="apijetrestoreinstance-method"></a><span data-ttu-id="fea81-103">Método API. JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="fea81-103">Api.JetRestoreInstance method</span></span>

<span data-ttu-id="fea81-104">Restaura e recupera um backup de streaming de uma instância do, incluindo todos os bancos de dados anexados.</span><span class="sxs-lookup"><span data-stu-id="fea81-104">Restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="fea81-105">Ele foi projetado para funcionar com um backup criado com a função [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) .</span><span class="sxs-lookup"><span data-stu-id="fea81-105">It is designed to work with a backup created with the [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) function.</span></span> <span data-ttu-id="fea81-106">Essa é a função de restauração mais simples e encapsulada.</span><span class="sxs-lookup"><span data-stu-id="fea81-106">This is the simplest and most encapsulated restore function.</span></span>

<span data-ttu-id="fea81-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fea81-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fea81-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fea81-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fea81-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fea81-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="fea81-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fea81-110">Parameters</span></span>

  - <span data-ttu-id="fea81-111">instance</span><span class="sxs-lookup"><span data-stu-id="fea81-111">instance</span></span>  
    <span data-ttu-id="fea81-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fea81-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="fea81-113">A instância a ser usada.</span><span class="sxs-lookup"><span data-stu-id="fea81-113">The instance to use.</span></span> <span data-ttu-id="fea81-114">A instância não deve ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="fea81-114">The instance should not be initialized.</span></span> <span data-ttu-id="fea81-115">A restauração dos arquivos irá inicializar a instância.</span><span class="sxs-lookup"><span data-stu-id="fea81-115">Restoring the files will initialize the instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="fea81-116">source</span><span class="sxs-lookup"><span data-stu-id="fea81-116">source</span></span>  
    <span data-ttu-id="fea81-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="fea81-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="fea81-118">Local do backup.</span><span class="sxs-lookup"><span data-stu-id="fea81-118">Location of the backup.</span></span> <span data-ttu-id="fea81-119">O backup deve ter sido criado com [JetBackupInstance (JET_INSTANCE, String, BackupGrbit JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="fea81-119">The backup should have been created with [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<!-- end list -->

  - <span data-ttu-id="fea81-120">destino</span><span class="sxs-lookup"><span data-stu-id="fea81-120">destination</span></span>  
    <span data-ttu-id="fea81-121">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="fea81-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="fea81-122">Nome da pasta em que os arquivos de banco de dados do conjunto de backup serão copiados e recuperados.</span><span class="sxs-lookup"><span data-stu-id="fea81-122">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="fea81-123">Se isso for definido como NULL, os arquivos de banco de dados serão copiados e recuperados em seu local original.</span><span class="sxs-lookup"><span data-stu-id="fea81-123">If this is set to null, the database files will be copied and recovered to their original location.</span></span>

<!-- end list -->

  - <span data-ttu-id="fea81-124">statusCallback</span><span class="sxs-lookup"><span data-stu-id="fea81-124">statusCallback</span></span>  
    <span data-ttu-id="fea81-125">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="fea81-125">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="fea81-126">Retorno de chamada de notificação de status opcional.</span><span class="sxs-lookup"><span data-stu-id="fea81-126">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="fea81-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fea81-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fea81-128">Referência</span><span class="sxs-lookup"><span data-stu-id="fea81-128">Reference</span></span>

[<span data-ttu-id="fea81-129">Classe de API</span><span class="sxs-lookup"><span data-stu-id="fea81-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fea81-130">Membros da API</span><span class="sxs-lookup"><span data-stu-id="fea81-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fea81-131">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fea81-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
