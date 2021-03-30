---
description: Especifica o valor do sinalizador de descarte de quadros no cabeçalho do grupo de imagens (GOP).
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Propriedade AVEncVideoHeaderDropFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825991"
---
# <a name="avencvideoheaderdropframe-property"></a><span data-ttu-id="793e6-103">Propriedade AVEncVideoHeaderDropFrame</span><span class="sxs-lookup"><span data-stu-id="793e6-103">AVEncVideoHeaderDropFrame property</span></span>

<span data-ttu-id="793e6-104">Especifica o valor do sinalizador de descarte de quadros no cabeçalho do grupo de imagens (GOP).</span><span class="sxs-lookup"><span data-stu-id="793e6-104">Specifies the value of drop-frame flag in the group of pictures (GOP) header.</span></span>

<span data-ttu-id="793e6-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="793e6-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="793e6-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="793e6-106">Data type</span></span>

<span data-ttu-id="793e6-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="793e6-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="793e6-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="793e6-108">Property GUID</span></span>

<span data-ttu-id="793e6-109">**CODECAPI \_ AVEncVideoHeaderDropFrame**</span><span class="sxs-lookup"><span data-stu-id="793e6-109">**CODECAPI\_AVEncVideoHeaderDropFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="793e6-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="793e6-110">Property value</span></span>

<span data-ttu-id="793e6-111">O valor dessa propriedade pode ser 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="793e6-111">The value of this property can be 0 or 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="793e6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="793e6-112">Remarks</span></span>

<span data-ttu-id="793e6-113">O modo de descarte de quadros é usado no vídeo NTSC para corrigir a discrepância entre o vídeo, que é de 29,97 quadros por segundo e a exibição do código de tempo, que é de 30 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="793e6-113">Drop-frame mode is used in NTSC video to correct the discrepancy between the video, which is 29.97 frames per second, and the time code display, which is 30 frames per second.</span></span> <span data-ttu-id="793e6-114">No modo de descarte de quadros, os números de quadro 00 e 01 são ignorados no início de cada minuto, exceto em minutos que são até múltiplos de dez (00, 10, 20 e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="793e6-114">In drop-frame mode, frame numbers 00 and 01 are skipped at the start of each minute, except for minutes that are even multiples of ten (00, 10, 20, and so forth).</span></span> <span data-ttu-id="793e6-115">Somente os números de quadro no código de tempo são descartados; nenhum quadro real foi removido.</span><span class="sxs-lookup"><span data-stu-id="793e6-115">Only the frame numbers in the time code are dropped; no actual frames are dropped.</span></span>

## <a name="requirements"></a><span data-ttu-id="793e6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="793e6-116">Requirements</span></span>



| <span data-ttu-id="793e6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="793e6-117">Requirement</span></span> | <span data-ttu-id="793e6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="793e6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="793e6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="793e6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="793e6-120">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="793e6-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="793e6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="793e6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="793e6-122">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="793e6-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="793e6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="793e6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="793e6-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="793e6-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="793e6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="793e6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="793e6-126">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="793e6-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="793e6-127">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="793e6-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




