---
description: Obtém a configuração do alto-falante para os canais de áudio no fluxo de bits de áudio.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Propriedade AVAudioChannelConfig (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ee1bc7897d92f7efa1b6d351d2f73c32867529
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009948"
---
# <a name="avaudiochannelconfig-property"></a><span data-ttu-id="15452-103">Propriedade AVAudioChannelConfig</span><span class="sxs-lookup"><span data-stu-id="15452-103">AVAudioChannelConfig property</span></span>

<span data-ttu-id="15452-104">Obtém a configuração do alto-falante para os canais de áudio no fluxo de bits de áudio.</span><span class="sxs-lookup"><span data-stu-id="15452-104">Gets the speaker configuration for the audio channels in the audio bit stream.</span></span>

<span data-ttu-id="15452-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="15452-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="15452-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="15452-106">Data type</span></span>

<span data-ttu-id="15452-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="15452-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="15452-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="15452-108">Property GUID</span></span>

<span data-ttu-id="15452-109">**CODECAPI \_ AVAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="15452-109">**CODECAPI\_AVAudioChannelConfig**</span></span>

## <a name="property-value"></a><span data-ttu-id="15452-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="15452-110">Property value</span></span>

<span data-ttu-id="15452-111">O valor dessa propriedade é uma operação OR dos membros da enumeração [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) .</span><span class="sxs-lookup"><span data-stu-id="15452-111">The value of this property is a bitwise OR of members of the [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="15452-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="15452-112">Remarks</span></span>

<span data-ttu-id="15452-113">O número de canais inclui o canal de baixo efeito de frequência (LFE), se presente.</span><span class="sxs-lookup"><span data-stu-id="15452-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="15452-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15452-114">Requirements</span></span>



| <span data-ttu-id="15452-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="15452-115">Requirement</span></span> | <span data-ttu-id="15452-116">Valor</span><span class="sxs-lookup"><span data-stu-id="15452-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15452-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15452-117">Minimum supported client</span></span><br/> | <span data-ttu-id="15452-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="15452-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="15452-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15452-119">Minimum supported server</span></span><br/> | <span data-ttu-id="15452-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="15452-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="15452-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15452-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="15452-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="15452-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15452-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="15452-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15452-124">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="15452-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="15452-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="15452-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




