---
description: Força o codificador a codificar o próximo quadro como um quadro-chave.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: Propriedade CODECAPI_AVEncVideoForceKeyFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812164"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a><span data-ttu-id="d747c-103">\_Propriedade CODECAPI AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="d747c-103">CODECAPI\_AVEncVideoForceKeyFrame property</span></span>

<span data-ttu-id="d747c-104">Força o codificador a codificar o próximo quadro como um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="d747c-104">Forces the encoder to code the next frame as a key frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="d747c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d747c-105">Data type</span></span>

<span data-ttu-id="d747c-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="d747c-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d747c-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="d747c-107">Property GUID</span></span>

<span data-ttu-id="d747c-108">**CODECAPI \_ AVEncVideoForceKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="d747c-108">**CODECAPI\_AVEncVideoForceKeyFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="d747c-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d747c-109">Property value</span></span>

<span data-ttu-id="d747c-110">Se o valor for diferente de zero, o codificador codificará o próximo quadro como um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="d747c-110">If the value is nonzero, the encoder will code the next frame as a key frame.</span></span> <span data-ttu-id="d747c-111">Se o valor for zero, o codificador selecionará se deseja codificar o próximo quadro como um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="d747c-111">If the value is zero, the encoder selects whether to encode the next frame as a key frame.</span></span>

<span data-ttu-id="d747c-112">Essa propriedade se aplica ao próximo quadro que o codificador recebe como entrada.</span><span class="sxs-lookup"><span data-stu-id="d747c-112">This property applies to the next frame that the encoder receives as input.</span></span> <span data-ttu-id="d747c-113">Para uma Media Foundation transformação (MFT), esse é o próximo quadro que é passado para o método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) .</span><span class="sxs-lookup"><span data-stu-id="d747c-113">For a Media Foundation transform (MFT), this is the next frame that is passed to the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method.</span></span> <span data-ttu-id="d747c-114">A configuração é redefinida como zero após o próximo quadro.</span><span class="sxs-lookup"><span data-stu-id="d747c-114">The setting resets to zero after the next frame.</span></span>

## <a name="remarks"></a><span data-ttu-id="d747c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d747c-115">Remarks</span></span>

<span data-ttu-id="d747c-116">Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="d747c-116">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d747c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d747c-117">Requirements</span></span>



| <span data-ttu-id="d747c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d747c-118">Requirement</span></span> | <span data-ttu-id="d747c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d747c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d747c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d747c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d747c-121">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d747c-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="d747c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d747c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d747c-123">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d747c-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d747c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d747c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d747c-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d747c-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d747c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d747c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d747c-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d747c-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d747c-128">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d747c-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

