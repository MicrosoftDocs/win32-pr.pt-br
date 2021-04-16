---
description: 'Saiba mais sobre: método API. JetGetLogInfoInstance'
title: Método API. JetGetLogInfoInstance
TOCTitle: 'JetGetLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100726
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85e252b74c47d3274fc83af59e3fb571906219fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750564"
---
# <a name="apijetgetloginfoinstance-method"></a><span data-ttu-id="7a6c7-103">Método API. JetGetLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="7a6c7-103">Api.JetGetLogInfoInstance method</span></span>

<span data-ttu-id="7a6c7-104">Usado durante um backup iniciado por [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar uma instância para obter os nomes dos arquivos de patch de banco de dados e dos LogFiles que devem se tornar parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="7a6c7-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database patch files and logfiles that should become part of the backup file set.</span></span> <span data-ttu-id="7a6c7-105">Esses arquivos podem ser abertos subsequentemente usando [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) e Read usando [JetReadFileInstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="7a6c7-105">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="7a6c7-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7a6c7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7a6c7-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7a6c7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7a6c7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a6c7-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="7a6c7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a6c7-109">Parameters</span></span>

  - <span data-ttu-id="7a6c7-110">instance</span><span class="sxs-lookup"><span data-stu-id="7a6c7-110">instance</span></span>  
    <span data-ttu-id="7a6c7-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7a6c7-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7a6c7-112">A instância para a qual obter as informações.</span><span class="sxs-lookup"><span data-stu-id="7a6c7-112">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a6c7-113">files</span><span class="sxs-lookup"><span data-stu-id="7a6c7-113">files</span></span>  
    <span data-ttu-id="7a6c7-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7a6c7-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7a6c7-115">Retorna uma lista de cadeias de caracteres terminadas em nulo que descrevem o conjunto de arquivos de patch de banco de dados e arquivos de log que devem ser parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="7a6c7-115">Returns a list of null terminated strings describing the set of database patch files and log files that should be a part of the backup file set.</span></span> <span data-ttu-id="7a6c7-116">A lista de cadeias de caracteres retornada nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro.</span><span class="sxs-lookup"><span data-stu-id="7a6c7-116">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="7a6c7-117">Cada cadeia de caracteres terminada em nulo é retornada em sequência seguida por um terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="7a6c7-117">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a6c7-118">maxChars</span><span class="sxs-lookup"><span data-stu-id="7a6c7-118">maxChars</span></span>  
    <span data-ttu-id="7a6c7-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7a6c7-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7a6c7-120">Número máximo de caracteres a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="7a6c7-120">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a6c7-121">actualChars</span><span class="sxs-lookup"><span data-stu-id="7a6c7-121">actualChars</span></span>  
    <span data-ttu-id="7a6c7-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7a6c7-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7a6c7-123">Tamanho real da lista de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7a6c7-123">Actual size of the file list.</span></span> <span data-ttu-id="7a6c7-124">Se for maior que maxChars, a lista foi truncada.</span><span class="sxs-lookup"><span data-stu-id="7a6c7-124">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a6c7-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a6c7-125">Remarks</span></span>

<span data-ttu-id="7a6c7-126">É importante observar que essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="7a6c7-126">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a6c7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a6c7-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7a6c7-128">Referência</span><span class="sxs-lookup"><span data-stu-id="7a6c7-128">Reference</span></span>

[<span data-ttu-id="7a6c7-129">Classe de API</span><span class="sxs-lookup"><span data-stu-id="7a6c7-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7a6c7-130">Membros da API</span><span class="sxs-lookup"><span data-stu-id="7a6c7-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7a6c7-131">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7a6c7-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
