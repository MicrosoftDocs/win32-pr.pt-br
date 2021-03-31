---
description: 'Saiba mais sobre: método API. JetGetTruncateLogInfoInstance'
title: Método API. JetGetTruncateLogInfoInstance
TOCTitle: 'JetGetTruncateLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettruncateloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100743
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc54d12796a724b382343c4a3514f03102df305f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171959"
---
# <a name="apijetgettruncateloginfoinstance-method"></a><span data-ttu-id="92a6f-103">Método API. JetGetTruncateLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="92a6f-103">Api.JetGetTruncateLogInfoInstance method</span></span>

<span data-ttu-id="92a6f-104">Usado durante um backup iniciado por [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar uma instância para obter os nomes dos arquivos de log de transações que podem ser excluídos com segurança depois que o backup for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="92a6f-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="92a6f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="92a6f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="92a6f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="92a6f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="92a6f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92a6f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTruncateLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetTruncateLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetTruncateLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="92a6f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92a6f-108">Parameters</span></span>

  - <span data-ttu-id="92a6f-109">instance</span><span class="sxs-lookup"><span data-stu-id="92a6f-109">instance</span></span>  
    <span data-ttu-id="92a6f-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="92a6f-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="92a6f-111">A instância para a qual obter as informações.</span><span class="sxs-lookup"><span data-stu-id="92a6f-111">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="92a6f-112">files</span><span class="sxs-lookup"><span data-stu-id="92a6f-112">files</span></span>  
    <span data-ttu-id="92a6f-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="92a6f-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="92a6f-114">Retorna uma lista de cadeias de caracteres terminadas em nulo que descrevem o conjunto de arquivos de log de banco de dados que podem ser excluídos com segurança após a conclusão do backup.</span><span class="sxs-lookup"><span data-stu-id="92a6f-114">Returns a list of null terminated strings describing the set of database log files that can be safely deleted after the backup completes.</span></span> <span data-ttu-id="92a6f-115">A lista de cadeias de caracteres retornada nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro.</span><span class="sxs-lookup"><span data-stu-id="92a6f-115">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="92a6f-116">Cada cadeia de caracteres terminada em nulo é retornada em sequência seguida por um terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="92a6f-116">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="92a6f-117">maxChars</span><span class="sxs-lookup"><span data-stu-id="92a6f-117">maxChars</span></span>  
    <span data-ttu-id="92a6f-118">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="92a6f-118">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="92a6f-119">Número máximo de caracteres a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="92a6f-119">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="92a6f-120">actualChars</span><span class="sxs-lookup"><span data-stu-id="92a6f-120">actualChars</span></span>  
    <span data-ttu-id="92a6f-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="92a6f-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="92a6f-122">Tamanho real da lista de arquivos.</span><span class="sxs-lookup"><span data-stu-id="92a6f-122">Actual size of the file list.</span></span> <span data-ttu-id="92a6f-123">Se for maior que maxChars, a lista foi truncada.</span><span class="sxs-lookup"><span data-stu-id="92a6f-123">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a6f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="92a6f-124">Remarks</span></span>

<span data-ttu-id="92a6f-125">É importante observar que essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="92a6f-125">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="92a6f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="92a6f-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="92a6f-127">Referência</span><span class="sxs-lookup"><span data-stu-id="92a6f-127">Reference</span></span>

[<span data-ttu-id="92a6f-128">Classe de API</span><span class="sxs-lookup"><span data-stu-id="92a6f-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="92a6f-129">Membros da API</span><span class="sxs-lookup"><span data-stu-id="92a6f-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="92a6f-130">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="92a6f-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
