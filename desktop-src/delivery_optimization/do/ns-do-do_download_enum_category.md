---
title: Estrutura de DO_DOWNLOAD_ENUM_CATEGORY
description: 'Usado por **IDOManager:: EnumDownloads** para filtrar a enumeração de downloads pelo valor da propriedade específica.'
keywords:
- Estrutura de DO_DOWNLOAD_ENUM_CATEGORY
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105798307"
---
# <a name="do_download_enum_category-structure"></a><span data-ttu-id="7ae91-104">Estrutura de DO_DOWNLOAD_ENUM_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="7ae91-104">DO_DOWNLOAD_ENUM_CATEGORY structure</span></span>

<span data-ttu-id="7ae91-105">A estrutura de **DO_DOWNLOAD_ENUM_CATEGORY** é usada por **IDOManager:: EnumDownloads** para filtrar a enumeração de downloads pelo valor da propriedade específica.</span><span class="sxs-lookup"><span data-stu-id="7ae91-105">The **DO_DOWNLOAD_ENUM_CATEGORY** structure is used by **IDOManager::EnumDownloads** to filter the downloads enumeration by the specific property's value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae91-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ae91-106">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a><span data-ttu-id="7ae91-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7ae91-107">Members</span></span>

`Property`

<span data-ttu-id="7ae91-108">O nome da propriedade a ser usada para a enumeração de download.</span><span class="sxs-lookup"><span data-stu-id="7ae91-108">The property name to be used for the download enumeration.</span></span> <span data-ttu-id="7ae91-109">Essas propriedades têm suporte para fins de enumeração.</span><span class="sxs-lookup"><span data-stu-id="7ae91-109">These properties are supported for enumeration purposes.</span></span>
- <span data-ttu-id="7ae91-110">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="7ae91-110">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="7ae91-111">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="7ae91-111">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="7ae91-112">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="7ae91-112">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="7ae91-113">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="7ae91-113">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="7ae91-114">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="7ae91-114">**DODownloadProperty_LocalPath**</span></span>

`Value`

<span data-ttu-id="7ae91-115">O valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7ae91-115">The property's value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae91-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ae91-116">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7ae91-117">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="7ae91-117">**Minimum supported client**</span></span> | <span data-ttu-id="7ae91-118">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="7ae91-118">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="7ae91-119">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="7ae91-119">**Minimum supported server**</span></span> | <span data-ttu-id="7ae91-120">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="7ae91-120">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="7ae91-121">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="7ae91-121">**Header**</span></span> | <span data-ttu-id="7ae91-122">Do. h</span><span class="sxs-lookup"><span data-stu-id="7ae91-122">Do.h</span></span> |
