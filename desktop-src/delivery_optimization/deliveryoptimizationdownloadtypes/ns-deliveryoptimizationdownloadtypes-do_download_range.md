---
title: Estrutura de DO_DOWNLOAD_RANGE
description: Identifica um único intervalo de bytes para baixar de um arquivo.
keywords:
- Estrutura de DO_DOWNLOAD_RANGE
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105791094"
---
# <a name="do_download_range-structure"></a><span data-ttu-id="078fe-104">Estrutura de DO_DOWNLOAD_RANGE</span><span class="sxs-lookup"><span data-stu-id="078fe-104">DO_DOWNLOAD_RANGE structure</span></span>

<span data-ttu-id="078fe-105">A estrutura de **DO_DOWNLOAD_RANGE** identifica um único intervalo de bytes para baixar de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="078fe-105">The **DO_DOWNLOAD_RANGE** structure identifies a single range of bytes to download from a file.</span></span> <span data-ttu-id="078fe-106">A estrutura de **DO_DOWNLOAD_RANGE** está incluída na estrutura **DO_DOWNLOAD_RANGES_INFO** para fornecer uma matriz de intervalos para download.</span><span class="sxs-lookup"><span data-stu-id="078fe-106">The **DO_DOWNLOAD_RANGE** structure is included within **DO_DOWNLOAD_RANGES_INFO** structure to provide an array of ranges to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="078fe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="078fe-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a><span data-ttu-id="078fe-108">Membros</span><span class="sxs-lookup"><span data-stu-id="078fe-108">Members</span></span>

`Offset`

<span data-ttu-id="078fe-109">Deslocamento de base zero para o início do intervalo de bytes a ser baixado de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="078fe-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

`Length`

<span data-ttu-id="078fe-110">O comprimento do intervalo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="078fe-110">The length of the range, in bytes.</span></span> <span data-ttu-id="078fe-111">Não especifique um comprimento de zero byte.</span><span class="sxs-lookup"><span data-stu-id="078fe-111">Do not specify a zero-byte length.</span></span> <span data-ttu-id="078fe-112">Para indicar que o intervalo se estende até o final do arquivo, especifique **DO_LENGTH_TO_EOF**.</span><span class="sxs-lookup"><span data-stu-id="078fe-112">To indicate that the range extends to the end of the file, specify **DO_LENGTH_TO_EOF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="078fe-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="078fe-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="078fe-114">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="078fe-114">**Minimum supported client**</span></span> | <span data-ttu-id="078fe-115">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="078fe-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="078fe-116">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="078fe-116">**Minimum supported server**</span></span> | <span data-ttu-id="078fe-117">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="078fe-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="078fe-118">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="078fe-118">**Header**</span></span> | <span data-ttu-id="078fe-119">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="078fe-119">DeliveryOptimizationDownloadTypes.h</span></span> |
