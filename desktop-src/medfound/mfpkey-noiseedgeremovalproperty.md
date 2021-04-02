---
description: Especifica se o codec deve tentar detectar bordas de quadro ruidosas e removê-las.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: Propriedade MFPKEY_NOISEEDGEREMOVAL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165385"
---
# <a name="mfpkey_noiseedgeremoval-property"></a><span data-ttu-id="d4c9b-103">\_Propriedade MFPKEY NOISEEDGEREMOVAL</span><span class="sxs-lookup"><span data-stu-id="d4c9b-103">MFPKEY\_NOISEEDGEREMOVAL Property</span></span>

<span data-ttu-id="d4c9b-104">Especifica se o codec deve tentar detectar bordas de quadro ruidosas e removê-las.</span><span class="sxs-lookup"><span data-stu-id="d4c9b-104">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d4c9b-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d4c9b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d4c9b-106">g \_ wszWMVCNoiseEdgeRemoval</span><span class="sxs-lookup"><span data-stu-id="d4c9b-106">g\_wszWMVCNoiseEdgeRemoval</span></span>

## <a name="data-type"></a><span data-ttu-id="d4c9b-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d4c9b-107">Data Type</span></span>

<span data-ttu-id="d4c9b-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="d4c9b-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="d4c9b-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="d4c9b-109">Default Value</span></span>

<span data-ttu-id="d4c9b-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="d4c9b-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="d4c9b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4c9b-111">Remarks</span></span>

<span data-ttu-id="d4c9b-112">Uma borda de quadro ruidosa é geralmente os dados de intervalo vertical em branco (VBI) de um quadro de televisão de difusão.</span><span class="sxs-lookup"><span data-stu-id="d4c9b-112">A noisy frame edge is usually the vertical blanking interval (VBI) data from a frame of broadcast television.</span></span> <span data-ttu-id="d4c9b-113">O VBI é o primeiro 21 linhas de varredura do quadro de televisão.</span><span class="sxs-lookup"><span data-stu-id="d4c9b-113">The VBI is the first 21 scan lines of the television frame.</span></span> <span data-ttu-id="d4c9b-114">Essas linhas de varredura não contêm dados de vídeo — elas contêm dados sobre a transmissão.</span><span class="sxs-lookup"><span data-stu-id="d4c9b-114">These scan lines do not contain video data—they contain data about the broadcast.</span></span> <span data-ttu-id="d4c9b-115">Quando um sinal de televisão é gravado por um cartão de captura, o VBI normalmente é removido do quadro.</span><span class="sxs-lookup"><span data-stu-id="d4c9b-115">When a television signal is recorded by a capture card, the VBI is usually removed from the frame.</span></span> <span data-ttu-id="d4c9b-116">A detecção de borda ruidosa e a correção executada pelo codec só podem corrigir uma borda com três ou menos linhas de ruído.</span><span class="sxs-lookup"><span data-stu-id="d4c9b-116">The noisy edge detection and correction performed by the codec can only correct an edge that has three or fewer lines of noise.</span></span> <span data-ttu-id="d4c9b-117">Se o vídeo capturado contiver mais de três linhas com ruído, haverá um problema com o hardware usado para capturar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="d4c9b-117">If captured video contains more than three noisy lines, there is a problem with the hardware used to capture the video.</span></span>

<span data-ttu-id="d4c9b-118">Se o codec for definido para remover bordas ruidosas, ele duplicará as linhas adjacentes à borda ruidosa para preencher o quadro.</span><span class="sxs-lookup"><span data-stu-id="d4c9b-118">If the codec is set to remove noisy edges, it duplicates lines adjacent to the noisy edge to fill in the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c9b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4c9b-119">Requirements</span></span>



| <span data-ttu-id="d4c9b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4c9b-120">Requirement</span></span> | <span data-ttu-id="d4c9b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d4c9b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c9b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4c9b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c9b-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d4c9b-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d4c9b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4c9b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c9b-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4c9b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d4c9b-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4c9b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4c9b-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4c9b-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4c9b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4c9b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c9b-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d4c9b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




