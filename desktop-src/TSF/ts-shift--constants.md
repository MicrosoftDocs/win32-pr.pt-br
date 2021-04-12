---
title: Constantes de TS_SHIFT_ (Textstor. h)
description: As \_ constantes TS SHIFT \_ são usadas pela interface IAnchor para manipulação de texto oculto e contagem de caracteres.
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369634"
---
# <a name="ts_shift_-constants"></a><span data-ttu-id="bacf5-103">Constantes do TS \_ SHIFT \_ \*</span><span class="sxs-lookup"><span data-stu-id="bacf5-103">TS\_SHIFT\_\* Constants</span></span>

<span data-ttu-id="bacf5-104">As \_ constantes TS SHIFT \_ \* são usadas pela interface **IAnchor** para manipulação de texto oculto e contagem de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bacf5-104">The TS\_Shift\_\* constants are used by the **IAnchor** interface for manipulation of hidden text and character counting.</span></span>



| <span data-ttu-id="bacf5-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="bacf5-105">Constant/value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="bacf5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bacf5-106">Description</span></span>                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <span data-ttu-id="bacf5-107"><dt>**TS \_ Contagem de DESLOCAMENTOs \_ \_ oculta**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="bacf5-107"><dt>**TS\_SHIFT\_COUNT\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="bacf5-108">Especifica que a âncora será deslocada para o próximo limite de região, incluindo o limite de uma região de texto oculta.</span><span class="sxs-lookup"><span data-stu-id="bacf5-108">Specifies that the anchor will be shifted to the next region boundary, including the boundary of a hidden text region.</span></span> <span data-ttu-id="bacf5-109">Se não estiver definido, a âncora será deslocada após qualquer texto oculto adjacente até que uma região de texto visível seja encontrada.</span><span class="sxs-lookup"><span data-stu-id="bacf5-109">If not set, the anchor will be shifted past any adjacent hidden text until a region of visible text is found.</span></span><br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <span data-ttu-id="bacf5-110"><dt>**TS \_ ALTERNAR \_ parada \_ oculta**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="bacf5-110"><dt>**TS\_SHIFT\_HALT\_HIDDEN**</dt> <dt>( 0x2 )</dt></span></span> </dl>    | <span data-ttu-id="bacf5-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="bacf5-111">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <span data-ttu-id="bacf5-112"><dt>**TS \_ Parada de deslocamento \_ \_ visível**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="bacf5-112"><dt>**TS\_SHIFT\_HALT\_VISIBLE**</dt> <dt>( 0x4 )</dt></span></span> </dl> | <span data-ttu-id="bacf5-113">Não usado.</span><span class="sxs-lookup"><span data-stu-id="bacf5-113">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <span data-ttu-id="bacf5-114"><dt>**TS \_ 0x8 \_ ( \_ somente contagem de deslocamento**</dt> <dt>)</dt></span><span class="sxs-lookup"><span data-stu-id="bacf5-114"><dt>**TS\_SHIFT\_COUNT\_ONLY**</dt> <dt>( 0x8 )</dt></span></span> </dl>       | <span data-ttu-id="bacf5-115">A âncora não é deslocada.</span><span class="sxs-lookup"><span data-stu-id="bacf5-115">The anchor is not shifted.</span></span><br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="bacf5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bacf5-116">Requirements</span></span>



| <span data-ttu-id="bacf5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bacf5-117">Requirement</span></span> | <span data-ttu-id="bacf5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bacf5-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bacf5-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bacf5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bacf5-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bacf5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bacf5-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bacf5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bacf5-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bacf5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bacf5-123">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="bacf5-123">Redistributable</span></span><br/>          | <span data-ttu-id="bacf5-124">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bacf5-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="bacf5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bacf5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bacf5-126"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="bacf5-126"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="bacf5-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="bacf5-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bacf5-128"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bacf5-128"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bacf5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bacf5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bacf5-130">IAnchor::ShiftRegion</span><span class="sxs-lookup"><span data-stu-id="bacf5-130">IAnchor::ShiftRegion</span></span>](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





