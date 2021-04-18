---
description: Especifica informações de quadro de referência de longo prazo (EPD) e retornadas no exemplo de saída.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: Atributo MFSampleExtension_LongTermReferenceFrameInfo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105767800"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a><span data-ttu-id="0928c-103">\_Atributo MFSampleExtension LongTermReferenceFrameInfo</span><span class="sxs-lookup"><span data-stu-id="0928c-103">MFSampleExtension\_LongTermReferenceFrameInfo attribute</span></span>

<span data-ttu-id="0928c-104">Especifica informações de quadro de referência de longo prazo (EPD) e retornadas no exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="0928c-104">Specifies Long Term Reference (LTR) frame info and is returned on the output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="0928c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0928c-105">Data type</span></span>

<span data-ttu-id="0928c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0928c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0928c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0928c-107">Remarks</span></span>

<span data-ttu-id="0928c-108">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="0928c-108">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="0928c-109">Os codificadores devem retornar esse atributo no exemplo de saída quando o aplicativo controla quadros EPD, que é especificado por [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span><span class="sxs-lookup"><span data-stu-id="0928c-109">Encoders shall return this attribute on the output sample when the application controls LTR frames, which is specified by [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

<span data-ttu-id="0928c-110">MFSampleExtension \_ LongTermReferenceFrameInfo retorna até dois campos.</span><span class="sxs-lookup"><span data-stu-id="0928c-110">MFSampleExtension\_LongTermReferenceFrameInfo returns up to two fields.</span></span>

<span data-ttu-id="0928c-111">O primeiro campo, bits \[ 0.. 15 \] , é *LongTermFrameIdx* associado ao quadro de saída se estiver marcado como um quadro EPD.</span><span class="sxs-lookup"><span data-stu-id="0928c-111">The first field, bits\[0..15\], is *LongTermFrameIdx* associated with the output frame if it is marked as a LTR frame.</span></span> <span data-ttu-id="0928c-112">O primeiro valor é 0xffff, se esse quadro de saída for um quadro de referência de curto prazo ou um quadro que não seja de referência.</span><span class="sxs-lookup"><span data-stu-id="0928c-112">The first value is 0xffff, if this output frame is a short term reference frame or a non-reference frame.</span></span>

<span data-ttu-id="0928c-113">O segundo campo, bits \[ 16.. 31 \] , é um bitmap que consiste em *MaxNumLTRFrames* muitos bits que indicam quais quadros EPD foram usados para codificar esse quadro de saída, começando do bit 16.</span><span class="sxs-lookup"><span data-stu-id="0928c-113">The second field, bits\[16..31\], is a bitmap consisting of *MaxNumLTRFrames* many bits that indicate which LTR frame(s) were used for encoding this output frame, starting from bit 16.</span></span> <span data-ttu-id="0928c-114">O restante dos bits deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="0928c-114">The rest of bits shall be set to 0.</span></span> <span data-ttu-id="0928c-115">O segundo valor será 0 se esse quadro de saída não for codificado usando quadros EPD.</span><span class="sxs-lookup"><span data-stu-id="0928c-115">The second value is 0 if this output frame is not encoded using any LTR frames.</span></span> <span data-ttu-id="0928c-116">*MaxNumLTRFrames* é o número máximo de quadros EPD definido por meio de [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span><span class="sxs-lookup"><span data-stu-id="0928c-116">*MaxNumLTRFrames* is the maximum number of LTR frames set through [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0928c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0928c-117">Requirements</span></span>



| <span data-ttu-id="0928c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0928c-118">Requirement</span></span> | <span data-ttu-id="0928c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0928c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0928c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0928c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0928c-121">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0928c-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="0928c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0928c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0928c-123">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="0928c-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0928c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0928c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0928c-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0928c-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0928c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0928c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0928c-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0928c-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




