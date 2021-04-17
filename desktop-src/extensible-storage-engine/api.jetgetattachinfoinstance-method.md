---
description: 'Saiba mais sobre: método API. JetGetAttachInfoInstance'
title: Método API. JetGetAttachInfoInstance
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94865042edf8b049b7140673a8aee1b4e2d91573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762204"
---
# <a name="apijetgetattachinfoinstance-method"></a><span data-ttu-id="0855a-103">Método API. JetGetAttachInfoInstance</span><span class="sxs-lookup"><span data-stu-id="0855a-103">Api.JetGetAttachInfoInstance method</span></span>

<span data-ttu-id="0855a-104">Usado durante um backup iniciado por [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar uma instância para obter os nomes dos arquivos de banco de dados que devem se tornar parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="0855a-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="0855a-105">Somente os bancos de dados atualmente anexados à instância usando [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) serão considerados.</span><span class="sxs-lookup"><span data-stu-id="0855a-105">Only databases that are currently attached to the instance using [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) will be considered.</span></span> <span data-ttu-id="0855a-106">Esses arquivos podem ser abertos subsequentemente usando [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) e Read usando [JetReadFileInstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="0855a-106">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="0855a-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0855a-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0855a-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0855a-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0855a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0855a-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="0855a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0855a-110">Parameters</span></span>

  - <span data-ttu-id="0855a-111">instance</span><span class="sxs-lookup"><span data-stu-id="0855a-111">instance</span></span>  
    <span data-ttu-id="0855a-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0855a-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="0855a-113">A instância para a qual obter as informações.</span><span class="sxs-lookup"><span data-stu-id="0855a-113">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="0855a-114">files</span><span class="sxs-lookup"><span data-stu-id="0855a-114">files</span></span>  
    <span data-ttu-id="0855a-115">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0855a-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0855a-116">Retorna uma lista de cadeias de caracteres terminadas em nulo que descrevem o conjunto de arquivos de banco de dados que deve ser parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="0855a-116">Returns a list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="0855a-117">A lista de cadeias de caracteres retornada nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro.</span><span class="sxs-lookup"><span data-stu-id="0855a-117">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="0855a-118">Cada cadeia de caracteres terminada em nulo é retornada em sequência seguida por um terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="0855a-118">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="0855a-119">maxChars</span><span class="sxs-lookup"><span data-stu-id="0855a-119">maxChars</span></span>  
    <span data-ttu-id="0855a-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0855a-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0855a-121">Número máximo de caracteres a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="0855a-121">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="0855a-122">actualChars</span><span class="sxs-lookup"><span data-stu-id="0855a-122">actualChars</span></span>  
    <span data-ttu-id="0855a-123">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0855a-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0855a-124">Tamanho real da lista de arquivos.</span><span class="sxs-lookup"><span data-stu-id="0855a-124">Actual size of the file list.</span></span> <span data-ttu-id="0855a-125">Se for maior que maxChars, a lista foi truncada.</span><span class="sxs-lookup"><span data-stu-id="0855a-125">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="0855a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="0855a-126">Remarks</span></span>

<span data-ttu-id="0855a-127">É importante observar que essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="0855a-127">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="0855a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0855a-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0855a-129">Referência</span><span class="sxs-lookup"><span data-stu-id="0855a-129">Reference</span></span>

[<span data-ttu-id="0855a-130">Classe de API</span><span class="sxs-lookup"><span data-stu-id="0855a-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0855a-131">Membros da API</span><span class="sxs-lookup"><span data-stu-id="0855a-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0855a-132">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0855a-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
