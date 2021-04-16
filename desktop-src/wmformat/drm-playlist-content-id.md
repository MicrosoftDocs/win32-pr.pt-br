---
title: Estrutura de DRM_PLAYLIST_CONTENT_ID (Drmexternals. h)
description: A estrutura de ID de conteúdo de playlist do DRM \_ \_ \_ contém informações sobre o conteúdo a ser copiado para o CD como parte de uma gravação de playlist.
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- Formato de mídia do Windows de estrutura de DRM_PLAYLIST_CONTENT_ID
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105765629"
---
# <a name="drm_playlist_content_id-structure"></a><span data-ttu-id="be9f6-105">\_Estrutura de \_ ID de conteúdo de playlist DRM \_</span><span class="sxs-lookup"><span data-stu-id="be9f6-105">DRM\_PLAYLIST\_CONTENT\_ID structure</span></span>

<span data-ttu-id="be9f6-106">A estrutura de ID de conteúdo de playlist do DRM contém informações sobre o conteúdo a ser copiado para o CD como parte de uma gravação de playlist. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be9f6-106">The **DRM\_PLAYLIST\_CONTENT\_ID** structure contains information about content that is to be copied to CD as part of a playlist burn.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9f6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be9f6-107">Syntax</span></span>


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a><span data-ttu-id="be9f6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="be9f6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="be9f6-109">**lpcwszV2Header**</span><span class="sxs-lookup"><span data-stu-id="be9f6-109">**lpcwszV2Header**</span></span>
</dt> <dd>

<span data-ttu-id="be9f6-110">Cabeçalho DRM.</span><span class="sxs-lookup"><span data-stu-id="be9f6-110">DRM header.</span></span> <span data-ttu-id="be9f6-111">Use esse membro se o conteúdo estiver protegido pelo Windows Media DRM versão 2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="be9f6-111">Use this member if the content is protected by Windows Media DRM version 2 or later.</span></span>

</dd> <dt>

<span data-ttu-id="be9f6-112">**lpcszV1KID**</span><span class="sxs-lookup"><span data-stu-id="be9f6-112">**lpcszV1KID**</span></span>
</dt> <dd>

<span data-ttu-id="be9f6-113">A ID da chave.</span><span class="sxs-lookup"><span data-stu-id="be9f6-113">Key ID.</span></span> <span data-ttu-id="be9f6-114">Use esse membro se o conteúdo estiver protegido pelo Windows Media DRM versão 1.</span><span class="sxs-lookup"><span data-stu-id="be9f6-114">Use this member if the content is protected by Windows Media DRM version 1.</span></span>

</dd> <dt>

<span data-ttu-id="be9f6-115">**pbOtherData**</span><span class="sxs-lookup"><span data-stu-id="be9f6-115">**pbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="be9f6-116">Buffer que contém dados suplementares.</span><span class="sxs-lookup"><span data-stu-id="be9f6-116">Buffer containing supplementary data.</span></span>

</dd> <dt>

<span data-ttu-id="be9f6-117">**cbOtherData**</span><span class="sxs-lookup"><span data-stu-id="be9f6-117">**cbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="be9f6-118">Tamanho do buffer **pbOtherData** em bytes.</span><span class="sxs-lookup"><span data-stu-id="be9f6-118">Size of the **pbOtherData** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="be9f6-119">**dwUniqueIDForSession**</span><span class="sxs-lookup"><span data-stu-id="be9f6-119">**dwUniqueIDForSession**</span></span>
</dt> <dd>

<span data-ttu-id="be9f6-120">Identificador exclusivo do conteúdo a ser usado na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="be9f6-120">Unique identifier for the content to be used in the current session.</span></span>

</dd> <dt>

<span data-ttu-id="be9f6-121">**dwValidFields**</span><span class="sxs-lookup"><span data-stu-id="be9f6-121">**dwValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="be9f6-122">**DWORD** que indica os campos válidos desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="be9f6-122">**DWORD** indicating the valid fields of this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be9f6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be9f6-123">Requirements</span></span>



| <span data-ttu-id="be9f6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="be9f6-124">Requirement</span></span> | <span data-ttu-id="be9f6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="be9f6-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="be9f6-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be9f6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="be9f6-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="be9f6-127">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="be9f6-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be9f6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="be9f6-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be9f6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="be9f6-130">Versão</span><span class="sxs-lookup"><span data-stu-id="be9f6-130">Version</span></span><br/>                  | <span data-ttu-id="be9f6-131">SDK do Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="be9f6-131">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="be9f6-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be9f6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="be9f6-133"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="be9f6-133"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9f6-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="be9f6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9f6-135">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="be9f6-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





