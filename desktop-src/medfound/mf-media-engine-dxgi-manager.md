---
description: Define o Gerenciador de Dispositivos de infraestrutura de gráficos do Microsoft DirectX (DXGI) no mecanismo de mídia.
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: Atributo MF_MEDIA_ENGINE_DXGI_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e731b5aa2449ae772427c6743ec4f97b5d7601
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105810799"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a><span data-ttu-id="ef714-103">\_Atributo de \_ Gerenciador de dxgi do mecanismo de mídia MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="ef714-103">MF\_MEDIA\_ENGINE\_DXGI\_MANAGER attribute</span></span>

<span data-ttu-id="ef714-104">Define o Gerenciador de Dispositivos de infraestrutura de gráficos do Microsoft DirectX (DXGI) no mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="ef714-104">Sets the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager on the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="ef714-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ef714-105">Data type</span></span>

<span data-ttu-id="ef714-106">**IMFDXGIDeviceManager \* *_ armazenado como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="ef714-106">**IMFDXGIDeviceManager\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="ef714-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="ef714-107">Get/set</span></span>

<span data-ttu-id="ef714-108">Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="ef714-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="ef714-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="ef714-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef714-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef714-110">Remarks</span></span>

<span data-ttu-id="ef714-111">O valor desse atributo é um ponteiro para a interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="ef714-111">The value of this attribute is a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="ef714-112">No modo de servidor de quadro, esse atributo permite que o mecanismo de mídia use a aceleração de hardware para decodificação de vídeo e processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ef714-112">In frame-server mode, this attribute enables the Media Engine to use hardware acceleration for video decoding and video processing.</span></span> <span data-ttu-id="ef714-113">Se o atributo não estiver definido, o mecanismo de mídia usará a decodificação e o processamento de software.</span><span class="sxs-lookup"><span data-stu-id="ef714-113">If the attribute is not set, the Media Engine uses software decoding and processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef714-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef714-114">Requirements</span></span>



| <span data-ttu-id="ef714-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef714-115">Requirement</span></span> | <span data-ttu-id="ef714-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ef714-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef714-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef714-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ef714-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ef714-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="ef714-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef714-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ef714-120">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ef714-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="ef714-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef714-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef714-122"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef714-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef714-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef714-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef714-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ef714-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ef714-125">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="ef714-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




