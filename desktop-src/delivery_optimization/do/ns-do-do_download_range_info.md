---
title: Estrutura de DO_DOWNLOAD_RANGE_INFO
description: Identifica uma matriz de intervalos de bytes a serem baixados de um arquivo.
keywords:
- Estrutura de DO_DOWNLOAD_RANGE_INFO
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365341"
---
# <a name="do_download_range_info-structure"></a><span data-ttu-id="f3e5f-104">Estrutura de DO_DOWNLOAD_RANGE_INFO</span><span class="sxs-lookup"><span data-stu-id="f3e5f-104">DO_DOWNLOAD_RANGE_INFO structure</span></span>

<span data-ttu-id="f3e5f-105">A estrutura de **DO_DOWNLOAD_RANGE_INFO** identifica uma matriz de intervalos de bytes a serem baixados de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3e5f-105">The **DO_DOWNLOAD_RANGE_INFO** structure identifies an array of ranges of bytes to download from a file.</span></span> <span data-ttu-id="f3e5f-106">Normalmente, ele é passado como um argumento opcional para a função **IDODownload:: Start** .</span><span class="sxs-lookup"><span data-stu-id="f3e5f-106">It is typically passed as an optional argument to the **IDODownload::Start** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e5f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3e5f-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a><span data-ttu-id="f3e5f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f3e5f-108">Members</span></span>

`RangeCount`

<span data-ttu-id="f3e5f-109">Número de elementos em intervalos.</span><span class="sxs-lookup"><span data-stu-id="f3e5f-109">Number of elements in Ranges.</span></span>

`Ranges`

<span data-ttu-id="f3e5f-110">Matriz de uma ou mais estruturas de **DO_DOWNLOAD_RANGE** que especificam os intervalos a serem baixados.</span><span class="sxs-lookup"><span data-stu-id="f3e5f-110">Array of one or more **DO_DOWNLOAD_RANGE** structures that specify the ranges to download.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3e5f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3e5f-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f3e5f-112">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="f3e5f-112">**Minimum supported client**</span></span> | <span data-ttu-id="f3e5f-113">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="f3e5f-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="f3e5f-114">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="f3e5f-114">**Minimum supported server**</span></span> | <span data-ttu-id="f3e5f-115">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="f3e5f-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="f3e5f-116">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="f3e5f-116">**Header**</span></span> | <span data-ttu-id="f3e5f-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="f3e5f-117">Do.h</span></span> |
