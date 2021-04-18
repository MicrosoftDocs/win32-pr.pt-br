---
description: As \_ constantes de sinalizador de bit LINEMEDIACONTROL descrevem um conjunto de operações genéricas em fluxos de mídia.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: Constantes de LINEMEDIACONTROL_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3241a3b5f4f8a0363f30ce7aefaded0c63fc4189
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780119"
---
# <a name="linemediacontrol_-constants"></a><span data-ttu-id="34ed8-103">\_Constantes LINEMEDIACONTROL</span><span class="sxs-lookup"><span data-stu-id="34ed8-103">LINEMEDIACONTROL\_ Constants</span></span>

<span data-ttu-id="34ed8-104">As constantes de sinalizador de bit **LINEMEDIACONTROL \_** descrevem um conjunto de operações genéricas em fluxos de mídia.</span><span class="sxs-lookup"><span data-stu-id="34ed8-104">The **LINEMEDIACONTROL\_** bit-flag constants describe a set of generic operations on media streams.</span></span> <span data-ttu-id="34ed8-105">As interpretações são determinadas pelo fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="34ed8-105">The interpretations are determined by the media stream.</span></span> <span data-ttu-id="34ed8-106">O dispositivo de linha deve ter o recurso de controle de mídia para que qualquer operação de controle de mídia seja efetiva.</span><span class="sxs-lookup"><span data-stu-id="34ed8-106">The line device must have the media-control capability for any media-control operation to be effective.</span></span>

<dl> <dt>

<span data-ttu-id="34ed8-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="34ed8-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34ed8-108">Nenhuma alteração é feita no fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="34ed8-108">No change is to be made to the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34ed8-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**Pausar LINEMEDIACONTROL \_**</span><span class="sxs-lookup"><span data-stu-id="34ed8-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL\_PAUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34ed8-110">Pause temporariamente o fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="34ed8-110">Temporarily pause the media stream.</span></span>

<span data-ttu-id="34ed8-111">A velocidade do fluxo de mídia é retornada para normal.</span><span class="sxs-lookup"><span data-stu-id="34ed8-111">The speed of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34ed8-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL \_ RATEDOWN**</span><span class="sxs-lookup"><span data-stu-id="34ed8-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL\_RATEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34ed8-113">A velocidade do fluxo de mídia é diminuída por uma quantidade definida pelo fluxo.</span><span class="sxs-lookup"><span data-stu-id="34ed8-113">The speed of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34ed8-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL \_ RATENORMAL**</span><span class="sxs-lookup"><span data-stu-id="34ed8-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL\_RATENORMAL**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34ed8-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL \_ RATEUP**</span><span class="sxs-lookup"><span data-stu-id="34ed8-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL\_RATEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34ed8-116">A velocidade do fluxo de mídia é aumentada por uma quantidade definida pelo fluxo.</span><span class="sxs-lookup"><span data-stu-id="34ed8-116">The speed of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34ed8-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**redefinição de LINEMEDIACONTROL \_**</span><span class="sxs-lookup"><span data-stu-id="34ed8-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**LINEMEDIACONTROL\_RESET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34ed8-118">Redefina o fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="34ed8-118">Reset the media stream.</span></span> <span data-ttu-id="34ed8-119">Equivalente a um fim de entrada.</span><span class="sxs-lookup"><span data-stu-id="34ed8-119">Equivalent to an end-of-input.</span></span> <span data-ttu-id="34ed8-120">Todos os buffers são liberados.</span><span class="sxs-lookup"><span data-stu-id="34ed8-120">All buffers are released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34ed8-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**retomar LINEMEDIACONTROL \_**</span><span class="sxs-lookup"><span data-stu-id="34ed8-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34ed8-122">Retomar um fluxo de mídia em pausa.</span><span class="sxs-lookup"><span data-stu-id="34ed8-122">Resume a paused media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34ed8-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL \_ Iniciar**</span><span class="sxs-lookup"><span data-stu-id="34ed8-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34ed8-124">Inicie o fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="34ed8-124">Start the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34ed8-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL \_ VOLUMEDOWN**</span><span class="sxs-lookup"><span data-stu-id="34ed8-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL\_VOLUMEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34ed8-126">A amplitude do fluxo de mídia é diminuída por uma quantidade definida pelo fluxo.</span><span class="sxs-lookup"><span data-stu-id="34ed8-126">The amplitude of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34ed8-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL \_ VOLUMENORMAL**</span><span class="sxs-lookup"><span data-stu-id="34ed8-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL\_VOLUMENORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34ed8-128">A amplitude do fluxo de mídia é retornada para normal.</span><span class="sxs-lookup"><span data-stu-id="34ed8-128">The amplitude of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34ed8-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL \_ VOLUMEUP**</span><span class="sxs-lookup"><span data-stu-id="34ed8-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL\_VOLUMEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34ed8-130">A amplitude do fluxo de mídia é aumentada por uma quantidade definida pelo fluxo.</span><span class="sxs-lookup"><span data-stu-id="34ed8-130">The amplitude of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34ed8-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="34ed8-131">Remarks</span></span>

<span data-ttu-id="34ed8-132">Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34ed8-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="34ed8-133">Os 16 bits de ordem inferior são reservados.</span><span class="sxs-lookup"><span data-stu-id="34ed8-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="34ed8-134">O controle de mídia é fornecido para melhorar o desempenho de ações em fluxos de mídia em resposta a eventos relacionados a telefonia.</span><span class="sxs-lookup"><span data-stu-id="34ed8-134">Media control is provided to improve performance of actions on media streams in response to telephony-related events.</span></span> <span data-ttu-id="34ed8-135">O aplicativo normalmente deve gerenciar um fluxo de mídia por meio da API específica da mídia.</span><span class="sxs-lookup"><span data-stu-id="34ed8-135">The application should normally manage a media stream through the media-specific API.</span></span> <span data-ttu-id="34ed8-136">A funcionalidade de controle de mídia fornecida aqui não se destina a substituir as APIs de mídia nativas.</span><span class="sxs-lookup"><span data-stu-id="34ed8-136">The media-control functionality provided here is not intended to replace the native media APIs.</span></span>

<span data-ttu-id="34ed8-137">As ações de controle de mídia podem ser associadas à detecção de dígitos, à detecção de tons, à transição para um estado de chamada e à detecção de um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="34ed8-137">Media-control actions can be associated with the detection of digits, the detection of tones, the transition into a call state, and the detection of a media type.</span></span> <span data-ttu-id="34ed8-138">Consulte os recursos do dispositivo de uma linha para determinar se o controle de mídia está disponível na linha.</span><span class="sxs-lookup"><span data-stu-id="34ed8-138">Consult a line's device capabilities to determine whether media control is available on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="34ed8-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34ed8-139">Requirements</span></span>



| <span data-ttu-id="34ed8-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="34ed8-140">Requirement</span></span> | <span data-ttu-id="34ed8-141">Valor</span><span class="sxs-lookup"><span data-stu-id="34ed8-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="34ed8-142">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="34ed8-142">TAPI version</span></span><br/> | <span data-ttu-id="34ed8-143">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="34ed8-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="34ed8-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34ed8-144">Header</span></span><br/>       | <dl> <span data-ttu-id="34ed8-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="34ed8-145"><dt>Tapi.h</dt></span></span> </dl> |



 

 




