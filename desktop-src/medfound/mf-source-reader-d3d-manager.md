---
description: Contém um ponteiro para o Gerenciador de Dispositivos do Microsoft Direct3D para o leitor de origem.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: Atributo MF_SOURCE_READER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828619"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a><span data-ttu-id="05903-103">\_Atributo de \_ Gerenciador de D3D do leitor de origem MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="05903-103">MF\_SOURCE\_READER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="05903-104">Contém um ponteiro para o Gerenciador de Dispositivos do Microsoft [Direct3D](direct3d-device-manager.md) para o [leitor de origem](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="05903-104">Contains a pointer to the Microsoft [Direct3D Device Manager](direct3d-device-manager.md) for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="05903-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="05903-105">Data type</span></span>

<span data-ttu-id="05903-106">**IDirect3DDeviceManager9 \* ou IMFDXGIDeviceManager \*** armazenado como \**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="05903-106">**IDirect3DDeviceManager9\* or IMFDXGIDeviceManager\*** stored as \**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="05903-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="05903-107">Get/set</span></span>

<span data-ttu-id="05903-108">Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="05903-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="05903-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="05903-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="05903-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="05903-110">Remarks</span></span>

<span data-ttu-id="05903-111">O valor desse atributo pode ser um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) ou um [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span><span class="sxs-lookup"><span data-stu-id="05903-111">The value of this attribute can be a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface or a [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span></span>

<span data-ttu-id="05903-112">Use este atributo para fornecer um dispositivo Direct3D para qualquer decodificador de vídeo carregado pelo leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="05903-112">Use this attribute to provide a Direct3D device for any video decoders loaded by the source reader.</span></span> <span data-ttu-id="05903-113">Se você definir esse atributo e o decodificador oferecer suporte ao Microsoft DirectX Video Acceleration (DXVA), o leitor de origem usará o dispositivo Direct3D para alocar buffers de vídeo.</span><span class="sxs-lookup"><span data-stu-id="05903-113">If you set this attribute and the decoder supports Microsoft DirectX Video Acceleration (DXVA), the source reader uses the Direct3D device to allocate video buffers.</span></span> <span data-ttu-id="05903-114">Esses buffers são compatíveis com o processador de vídeo DXVA 2.</span><span class="sxs-lookup"><span data-stu-id="05903-114">These buffers are compatible with the DXVA 2 video processor.</span></span> <span data-ttu-id="05903-115">(Consulte [processamento de vídeo de DXVA](dxva-video-processing.md).)</span><span class="sxs-lookup"><span data-stu-id="05903-115">(See [DXVA Video Processing](dxva-video-processing.md).)</span></span>

<span data-ttu-id="05903-116">Use este atributo com as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="05903-116">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="05903-117">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="05903-117">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="05903-118">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="05903-118">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="05903-119">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="05903-119">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="05903-120">Normalmente, você definiria esse atributo se estiver usando o leitor de origem para obter quadros de vídeo decodificados e usar o Direct3D para exibir os quadros.</span><span class="sxs-lookup"><span data-stu-id="05903-120">Typically you would set this attribute if you are using the source reader to get decoded video frames and using Direct3D to display the frames.</span></span> <span data-ttu-id="05903-121">Definir esse atributo permite que o decodificador use DXVA.</span><span class="sxs-lookup"><span data-stu-id="05903-121">Setting this attribute enables the decoder to use DXVA.</span></span>

<span data-ttu-id="05903-122">Você não definirá esse atributo se:</span><span class="sxs-lookup"><span data-stu-id="05903-122">You would not set this attribute if:</span></span>

-   <span data-ttu-id="05903-123">Você está usando o leitor de origem para processar somente áudio e não vídeo.</span><span class="sxs-lookup"><span data-stu-id="05903-123">You are using the source reader to process audio only and not video.</span></span>
-   <span data-ttu-id="05903-124">Você está obtendo vídeo compactado do leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="05903-124">You are getting compressed video from the source reader.</span></span> <span data-ttu-id="05903-125">Nesse caso, o leitor de origem não cria um decodificador.</span><span class="sxs-lookup"><span data-stu-id="05903-125">In that case, the source reader does not create a decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="05903-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05903-126">Requirements</span></span>



| <span data-ttu-id="05903-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="05903-127">Requirement</span></span> | <span data-ttu-id="05903-128">Valor</span><span class="sxs-lookup"><span data-stu-id="05903-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="05903-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05903-129">Minimum supported client</span></span><br/> | <span data-ttu-id="05903-130">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="05903-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="05903-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05903-131">Minimum supported server</span></span><br/> | <span data-ttu-id="05903-132">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="05903-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="05903-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05903-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="05903-134"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="05903-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05903-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="05903-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05903-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05903-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="05903-137">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="05903-137">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="05903-138">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="05903-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




