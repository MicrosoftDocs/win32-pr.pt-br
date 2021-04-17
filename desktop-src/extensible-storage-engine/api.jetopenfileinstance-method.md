---
description: 'Saiba mais sobre: método API. JetOpenFileInstance'
title: Método API. JetOpenFileInstance
TOCTitle: 'JetOpenFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.JET_HANDLE@,System.Int64@,System.Int64@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopenfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100767
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b58b3a426fd2eb7e33cce1f5f539418bcc993ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812018"
---
# <a name="apijetopenfileinstance-method"></a><span data-ttu-id="c8601-103">Método API. JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="c8601-103">Api.JetOpenFileInstance method</span></span>

<span data-ttu-id="c8601-104">Abre um banco de dados anexado, um arquivo de patch de banco de dados ou um arquivo de log de transações de uma instância ativa com a finalidade de executar um backup difuso de streaming.</span><span class="sxs-lookup"><span data-stu-id="c8601-104">Opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="c8601-105">Os dados desses arquivos podem, subsequentemente, ser lidos por meio do identificador retornado usando JetReadFileInstance.</span><span class="sxs-lookup"><span data-stu-id="c8601-105">The data from these files can subsequently be read through the returned handle using JetReadFileInstance.</span></span> <span data-ttu-id="c8601-106">O identificador retornado deve ser fechado usando JetCloseFileInstance.</span><span class="sxs-lookup"><span data-stu-id="c8601-106">The returned handle must be closed using JetCloseFileInstance.</span></span> <span data-ttu-id="c8601-107">Um backup externo da instância deve ter sido iniciado anteriormente usando JetBeginExternalBackupInstance.</span><span class="sxs-lookup"><span data-stu-id="c8601-107">An external backup of the instance must have been previously initiated using JetBeginExternalBackupInstance.</span></span>

<span data-ttu-id="c8601-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c8601-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c8601-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c8601-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c8601-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8601-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenFileInstance ( _
    instance As JET_INSTANCE, _
    file As String, _
    <OutAttribute> ByRef handle As JET_HANDLE, _
    <OutAttribute> ByRef fileSizeLow As Long, _
    <OutAttribute> ByRef fileSizeHigh As Long _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As String
Dim handle As JET_HANDLE
Dim fileSizeLow As Long
Dim fileSizeHigh As LongApi.JetOpenFileInstance(instance, _
    file, handle, fileSizeLow, fileSizeHigh)
```

``` csharp
public static void JetOpenFileInstance(
    JET_INSTANCE instance,
    string file,
    out JET_HANDLE handle,
    out long fileSizeLow,
    out long fileSizeHigh
)
```

#### <a name="parameters"></a><span data-ttu-id="c8601-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8601-111">Parameters</span></span>

  - <span data-ttu-id="c8601-112">instance</span><span class="sxs-lookup"><span data-stu-id="c8601-112">instance</span></span>  
    <span data-ttu-id="c8601-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c8601-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="c8601-114">A instância a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c8601-114">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c8601-115">arquivo</span><span class="sxs-lookup"><span data-stu-id="c8601-115">file</span></span>  
    <span data-ttu-id="c8601-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c8601-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c8601-117">O arquivo a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="c8601-117">The file to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="c8601-118">processamento</span><span class="sxs-lookup"><span data-stu-id="c8601-118">handle</span></span>  
    <span data-ttu-id="c8601-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c8601-119">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="c8601-120">Retorna um identificador para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c8601-120">Returns a handle to the file.</span></span>

<!-- end list -->

  - <span data-ttu-id="c8601-121">fileSizeLow</span><span class="sxs-lookup"><span data-stu-id="c8601-121">fileSizeLow</span></span>  
    <span data-ttu-id="c8601-122">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="c8601-122">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="c8601-123">Retorna os 32 bits menos significativos do tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c8601-123">Returns the least significant 32 bits of the file size.</span></span>

<!-- end list -->

  - <span data-ttu-id="c8601-124">fileSizeHigh</span><span class="sxs-lookup"><span data-stu-id="c8601-124">fileSizeHigh</span></span>  
    <span data-ttu-id="c8601-125">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="c8601-125">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="c8601-126">Retorna os 32 bits mais significativos do tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c8601-126">Returns the most significant 32 bits of the file size.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8601-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8601-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c8601-128">Referência</span><span class="sxs-lookup"><span data-stu-id="c8601-128">Reference</span></span>

[<span data-ttu-id="c8601-129">Classe de API</span><span class="sxs-lookup"><span data-stu-id="c8601-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c8601-130">Membros da API</span><span class="sxs-lookup"><span data-stu-id="c8601-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c8601-131">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c8601-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
