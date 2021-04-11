---
description: Especifica se o mecanismo de captura usa a DXVA (aceleração de vídeo do DirectX) para decodificação de vídeo.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: Atributo MF_CAPTURE_ENGINE_DISABLE_DXVA (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296436"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a><span data-ttu-id="3e9b5-103">\_Mecanismo de captura MF \_ \_ desabilitar \_ atributo DXVA</span><span class="sxs-lookup"><span data-stu-id="3e9b5-103">MF\_CAPTURE\_ENGINE\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="3e9b5-104">Especifica se o mecanismo de captura usa a DXVA (aceleração de vídeo do DirectX) para decodificação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3e9b5-104">Specifies whether the capture engine uses DirectX Video Acceleration (DXVA) for video decoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="3e9b5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3e9b5-105">Data type</span></span>

<span data-ttu-id="3e9b5-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="3e9b5-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3e9b5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e9b5-107">Remarks</span></span>

<span data-ttu-id="3e9b5-108">Esse atributo se aplicará se as seguintes condições forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="3e9b5-108">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="3e9b5-109">O mecanismo de captura decodifica um fluxo de vídeo compactado do dispositivo de captura (por exemplo, se o dispositivo de captura produzir o vídeo H. 264).</span><span class="sxs-lookup"><span data-stu-id="3e9b5-109">The capture engine decodes a compressed video stream from the capture device (for example, if the capture device outputs H.264 video).</span></span>
-   <span data-ttu-id="3e9b5-110">O decodificador de vídeo dá suporte à decodificação acelerada por hardware usando DXVA.</span><span class="sxs-lookup"><span data-stu-id="3e9b5-110">The video decoder supports hardware-accelerated decoding using DXVA.</span></span>
-   <span data-ttu-id="3e9b5-111">O aplicativo usa o atributo de [Gerenciador de D3D do \_ mecanismo de captura \_ \_ \_ MF](mf-capture-engine-d3d-manager.md) para definir o Gerenciador de dispositivos dxgi no mecanismo de captura.</span><span class="sxs-lookup"><span data-stu-id="3e9b5-111">The application uses the [MF\_CAPTURE\_ENGINE\_D3D\_MANAGER](mf-capture-engine-d3d-manager.md) attribute to set the DXGI Device Manager on the capture engine.</span></span>

<span data-ttu-id="3e9b5-112">Caso contrário, esse atributo será ignorado.</span><span class="sxs-lookup"><span data-stu-id="3e9b5-112">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="3e9b5-113">Esse atributo permite que o aplicativo desabilite o DXVA enquanto estiver decodificando as superfícies do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3e9b5-113">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="3e9b5-114">O valor padrão desse atributo é **false**, o que significa que a decodificação de DXVA está habilitada quando disponível.</span><span class="sxs-lookup"><span data-stu-id="3e9b5-114">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e9b5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e9b5-115">Requirements</span></span>



| <span data-ttu-id="3e9b5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e9b5-116">Requirement</span></span> | <span data-ttu-id="3e9b5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3e9b5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9b5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e9b5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3e9b5-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3e9b5-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="3e9b5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e9b5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3e9b5-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3e9b5-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3e9b5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e9b5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e9b5-123"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e9b5-123"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e9b5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e9b5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e9b5-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e9b5-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3e9b5-126">Atributos do mecanismo de captura</span><span class="sxs-lookup"><span data-stu-id="3e9b5-126">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="3e9b5-127">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="3e9b5-127">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




