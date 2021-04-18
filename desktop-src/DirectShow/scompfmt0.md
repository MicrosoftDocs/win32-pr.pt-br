---
description: Contém informações de formato para a recompactação inteligente.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: Estrutura SCompFmt0 (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758428"
---
# <a name="scompfmt0-structure"></a><span data-ttu-id="a3810-103">Estrutura SCompFmt0</span><span class="sxs-lookup"><span data-stu-id="a3810-103">SCompFmt0 structure</span></span>

> [!Note]  
> <span data-ttu-id="a3810-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="a3810-104">\[Deprecated.</span></span> <span data-ttu-id="a3810-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a3810-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a3810-106">Contém informações de formato para a recompactação inteligente.</span><span class="sxs-lookup"><span data-stu-id="a3810-106">Contains format information for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3810-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3810-107">Syntax</span></span>


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a><span data-ttu-id="a3810-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a3810-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a3810-109">**nFormatId**</span><span class="sxs-lookup"><span data-stu-id="a3810-109">**nFormatId**</span></span>
</dt> <dd>

<span data-ttu-id="a3810-110">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a3810-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a3810-111">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="a3810-111">**MediaType**</span></span>
</dt> <dd>

<span data-ttu-id="a3810-112">[**Am \_ Estrutura do \_ tipo de mídia**](/windows/win32/api/strmif/ns-strmif-am_media_type) que descreve o formato de compactação.</span><span class="sxs-lookup"><span data-stu-id="a3810-112">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that describes the compression format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3810-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3810-113">Requirements</span></span>



| <span data-ttu-id="a3810-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3810-114">Requirement</span></span> | <span data-ttu-id="a3810-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a3810-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3810-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3810-116">Header</span></span><br/> | <dl> <span data-ttu-id="a3810-117"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3810-117"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3810-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3810-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3810-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="a3810-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[<span data-ttu-id="a3810-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="a3810-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




