---
description: Define um ponteiro para o Gerenciador de Dispositivos DXGI no mecanismo de captura.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: Atributo MF_CAPTURE_ENGINE_D3D_MANAGER (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090696"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a><span data-ttu-id="6552f-103">\_Atributo do \_ Gerenciador de D3D do mecanismo de captura MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="6552f-103">MF\_CAPTURE\_ENGINE\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="6552f-104">Define um ponteiro para o Gerenciador de Dispositivos DXGI no mecanismo de captura.</span><span class="sxs-lookup"><span data-stu-id="6552f-104">Sets a pointer to the DXGI Device Manager on the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="6552f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6552f-105">Data type</span></span>

<span data-ttu-id="6552f-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="6552f-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="6552f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6552f-107">Remarks</span></span>

<span data-ttu-id="6552f-108">O valor desse atributo é um ponteiro para a interface [_ *IMFDXGIDeviceManager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="6552f-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span> <span data-ttu-id="6552f-109">Esse atributo permite que o mecanismo de captura aloque quadros de vídeo usando superfícies DXGI e use aceleração de hardware para decodificação e processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6552f-109">This attribute enables the capture engine to allocate video frames using DXGI surfaces, and to use hardware acceleration for decoding and video processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6552f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6552f-110">Requirements</span></span>



| <span data-ttu-id="6552f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="6552f-111">Requirement</span></span> | <span data-ttu-id="6552f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="6552f-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6552f-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6552f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6552f-114">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6552f-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="6552f-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6552f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6552f-116">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6552f-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6552f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6552f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6552f-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="6552f-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6552f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="6552f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6552f-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6552f-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6552f-121">Atributos do mecanismo de captura</span><span class="sxs-lookup"><span data-stu-id="6552f-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="6552f-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="6552f-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




