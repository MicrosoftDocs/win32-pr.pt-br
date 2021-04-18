---
title: Estrutura de DO_DOWNLOAD_STATUS
description: Usado para obter o status de um download específico.
keywords:
- Estrutura de DO_DOWNLOAD_STATUS
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105785975"
---
# <a name="do_download_status-structure"></a><span data-ttu-id="1b438-104">Estrutura de DO_DOWNLOAD_STATUS</span><span class="sxs-lookup"><span data-stu-id="1b438-104">DO_DOWNLOAD_STATUS structure</span></span>

<span data-ttu-id="1b438-105">A estrutura de **DO_DOWNLOAD_STATUS** é usada para obter o status de um download específico.</span><span class="sxs-lookup"><span data-stu-id="1b438-105">The **DO_DOWNLOAD_STATUS** structure is used to obtain the status of a specific download.</span></span> <span data-ttu-id="1b438-106">É obtido chamando a função **IDODownload:: GetStatus** .</span><span class="sxs-lookup"><span data-stu-id="1b438-106">It is obtained by calling the **IDODownload::GetStatus** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b438-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b438-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a><span data-ttu-id="1b438-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1b438-108">Members</span></span>

`BytesTotal`

<span data-ttu-id="1b438-109">O número total de bytes a serem baixados.</span><span class="sxs-lookup"><span data-stu-id="1b438-109">The total number of bytes to download.</span></span>

`BytesTransferred`

<span data-ttu-id="1b438-110">O número de bytes que já foram baixados.</span><span class="sxs-lookup"><span data-stu-id="1b438-110">The number of bytes that have already been downloaded.</span></span>

`State`

<span data-ttu-id="1b438-111">O estado de download atual, conforme definido pela enumeração **Dodownloadstate** .</span><span class="sxs-lookup"><span data-stu-id="1b438-111">The current download state as defined by the **DODownloadState** enumeration.</span></span>

`Error`

<span data-ttu-id="1b438-112">As informações de erro (se houver) que estão associadas ao download atual.</span><span class="sxs-lookup"><span data-stu-id="1b438-112">The error information (if it exists) that is associated with the current download.</span></span>

`ExtendedError`

<span data-ttu-id="1b438-113">As informações de erro estendidas (se existir) que estão associadas ao download atual.</span><span class="sxs-lookup"><span data-stu-id="1b438-113">The extended error information (if it exists) that is associated with the current download.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b438-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b438-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1b438-115">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="1b438-115">**Minimum supported client**</span></span> | <span data-ttu-id="1b438-116">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="1b438-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="1b438-117">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="1b438-117">**Minimum supported server**</span></span> | <span data-ttu-id="1b438-118">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="1b438-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="1b438-119">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="1b438-119">**Header**</span></span> | <span data-ttu-id="1b438-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="1b438-120">Do.h</span></span> |
