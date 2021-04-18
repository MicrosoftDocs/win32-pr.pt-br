---
description: Indica se um flash foi disparado para o quadro capturado.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: Atributo MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810767"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a><span data-ttu-id="17d20-103">\_ \_ \_ \_ Atributo flash do quadro de fotos de metadados do MF Capture \_</span><span class="sxs-lookup"><span data-stu-id="17d20-103">MF\_CAPTURE\_METADATA\_PHOTO\_FRAME\_FLASH attribute</span></span>

<span data-ttu-id="17d20-104">Indica se um flash foi disparado para o quadro capturado.</span><span class="sxs-lookup"><span data-stu-id="17d20-104">Indicates if a flash was triggered for the captured frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="17d20-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="17d20-105">Data type</span></span>

<span data-ttu-id="17d20-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="17d20-106">**UINT32**</span></span>



| <span data-ttu-id="17d20-107">Valor</span><span class="sxs-lookup"><span data-stu-id="17d20-107">Value</span></span>                                                                               | <span data-ttu-id="17d20-108">Significado</span><span class="sxs-lookup"><span data-stu-id="17d20-108">Meaning</span></span>                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="17d20-109"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="17d20-109"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="17d20-110">Um flash não foi disparado neste quadro.</span><span class="sxs-lookup"><span data-stu-id="17d20-110">A flash was not triggered on this frame.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="17d20-111"><dt>diferente de zero</dt></span><span class="sxs-lookup"><span data-stu-id="17d20-111"><dt>non-zero</dt></span></span> </dl> | <span data-ttu-id="17d20-112">Um flash foi disparado neste quadro.</span><span class="sxs-lookup"><span data-stu-id="17d20-112">A flash was triggered on this frame.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="17d20-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="17d20-113"><dt>1</dt></span></span> </dl>        | <span data-ttu-id="17d20-114">Reservado</span><span class="sxs-lookup"><span data-stu-id="17d20-114">Reserved</span></span><br/> <span data-ttu-id="17d20-115">Não verifique explicitamente um valor de 1.</span><span class="sxs-lookup"><span data-stu-id="17d20-115">Do not explicitly check for a value of 1.</span></span> <span data-ttu-id="17d20-116">Os aplicativos só devem verificar! = 0 para indicar se um flash foi disparado.</span><span class="sxs-lookup"><span data-stu-id="17d20-116">Applications should only check for !=0 to indicate if a flash was triggered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17d20-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17d20-117">Requirements</span></span>



| <span data-ttu-id="17d20-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="17d20-118">Requirement</span></span> | <span data-ttu-id="17d20-119">Valor</span><span class="sxs-lookup"><span data-stu-id="17d20-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17d20-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17d20-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17d20-121">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="17d20-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="17d20-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17d20-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17d20-123">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="17d20-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="17d20-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17d20-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="17d20-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="17d20-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17d20-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="17d20-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d20-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="17d20-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




