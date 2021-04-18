---
description: A tabela a seguir lista os GUIDs (identificadores globais exclusivos) definidos para as categorias do Microsoft DirectX Media Object (DMO). Essas GUIDs são definidas no arquivo de cabeçalho Dmoreg. h e exportadas pela biblioteca Dmoguids. lib.
ms.assetid: d67debd0-8ecb-41ab-bc6c-b27cba97c65a
title: GUIDs DMO (Dmoreg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10d5bd917d6368d398362e76ffa9ea8255933ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750640"
---
# <a name="dmo-guids"></a><span data-ttu-id="744cf-104">GUIDs de DMO</span><span class="sxs-lookup"><span data-stu-id="744cf-104">DMO GUIDs</span></span>

<span data-ttu-id="744cf-105">A tabela a seguir lista os GUIDs (identificadores globais exclusivos) definidos para as categorias do Microsoft DirectX Media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="744cf-105">The following table lists the globally unique identifiers (GUIDs) defined for Microsoft DirectX Media Object (DMO) categories.</span></span> <span data-ttu-id="744cf-106">Essas GUIDs são definidas no arquivo de cabeçalho Dmoreg. h e exportadas pela biblioteca Dmoguids. lib.</span><span class="sxs-lookup"><span data-stu-id="744cf-106">These GUIDs are defined in the header file Dmoreg.h and exported by the Dmoguids.lib library.</span></span>

<span data-ttu-id="744cf-107">Para enumerar o DMOs registrado em uma categoria, passe o GUID correspondente para a função [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) .</span><span class="sxs-lookup"><span data-stu-id="744cf-107">To enumerate the DMOs registered in a category, pass the corresponding GUID to the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span>



| <span data-ttu-id="744cf-108">GUID</span><span class="sxs-lookup"><span data-stu-id="744cf-108">GUID</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="744cf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="744cf-109">Description</span></span>                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------|
| <span id="DMOCATEGORY_AUDIO_DECODER"></span><span id="dmocategory_audio_decoder"></span><dl> <span data-ttu-id="744cf-110"><dt>**\_decodificador de áudio DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="744cf-110"><dt>**DMOCATEGORY\_AUDIO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="744cf-111">Decodificador de áudio</span><span class="sxs-lookup"><span data-stu-id="744cf-111">Audio decoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_EFFECT"></span><span id="dmocategory_audio_effect"></span><dl> <span data-ttu-id="744cf-112"><dt>**\_efeito de áudio DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="744cf-112"><dt>**DMOCATEGORY\_AUDIO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="744cf-113">Efeito de áudio</span><span class="sxs-lookup"><span data-stu-id="744cf-113">Audio effect</span></span><br/>         |
| <span id="DMOCATEGORY_AUDIO_ENCODER"></span><span id="dmocategory_audio_encoder"></span><dl> <span data-ttu-id="744cf-114"><dt>**\_codificador de áudio DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="744cf-114"><dt>**DMOCATEGORY\_AUDIO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="744cf-115">Codificador de áudio</span><span class="sxs-lookup"><span data-stu-id="744cf-115">Audio encoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_DECODER"></span><span id="dmocategory_video_decoder"></span><dl> <span data-ttu-id="744cf-116"><dt>**\_decodificador de vídeo DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="744cf-116"><dt>**DMOCATEGORY\_VIDEO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="744cf-117">Decodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="744cf-117">Video decoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_EFFECT"></span><span id="dmocategory_video_effect"></span><dl> <span data-ttu-id="744cf-118"><dt>**\_efeito de vídeo DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="744cf-118"><dt>**DMOCATEGORY\_VIDEO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="744cf-119">Efeito de vídeo</span><span class="sxs-lookup"><span data-stu-id="744cf-119">Video effect</span></span><br/>         |
| <span id="DMOCATEGORY_VIDEO_ENCODER"></span><span id="dmocategory_video_encoder"></span><dl> <span data-ttu-id="744cf-120"><dt>**\_codificador de vídeo DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="744cf-120"><dt>**DMOCATEGORY\_VIDEO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="744cf-121">Codificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="744cf-121">Video encoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_CAPTURE_EFFECT"></span><span id="dmocategory_audio_capture_effect"></span><dl> <span data-ttu-id="744cf-122"><dt>**\_efeito de \_ captura de áudio DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="744cf-122"><dt>**DMOCATEGORY\_AUDIO\_CAPTURE\_EFFECT**</dt></span></span> </dl> | <span data-ttu-id="744cf-123">Efeito de captura de áudio</span><span class="sxs-lookup"><span data-stu-id="744cf-123">Audio capture effect</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="744cf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="744cf-124">Requirements</span></span>



| <span data-ttu-id="744cf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="744cf-125">Requirement</span></span> | <span data-ttu-id="744cf-126">Valor</span><span class="sxs-lookup"><span data-stu-id="744cf-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="744cf-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="744cf-127">Header</span></span><br/> | <dl> <span data-ttu-id="744cf-128"><dt>Dmoreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="744cf-128"><dt>Dmoreg.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="744cf-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="744cf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="744cf-130">Constantes do DMO</span><span class="sxs-lookup"><span data-stu-id="744cf-130">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




