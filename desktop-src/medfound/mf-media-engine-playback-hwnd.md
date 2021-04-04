---
description: Define um identificador para uma janela de reprodução de vídeo para o mecanismo de mídia.
ms.assetid: 63889D81-12C5-47C1-B52A-6358E68830C3
title: Atributo MF_MEDIA_ENGINE_PLAYBACK_HWND (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6a9d38d40b04b32244f48289d3334199a7e035
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930118"
---
# <a name="mf_media_engine_playback_hwnd-attribute"></a><span data-ttu-id="b2022-103">\_ \_ \_ Atributo HWND de reprodução do mecanismo de mídia MF \_</span><span class="sxs-lookup"><span data-stu-id="b2022-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND attribute</span></span>

<span data-ttu-id="b2022-104">Define um identificador para uma janela de reprodução de vídeo para o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b2022-104">Sets a handle to a video playback window for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="b2022-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b2022-105">Data type</span></span>

<span data-ttu-id="b2022-106">**HWND** armazenado como **UINT64**</span><span class="sxs-lookup"><span data-stu-id="b2022-106">**HWND** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="b2022-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="b2022-107">Get/set</span></span>

<span data-ttu-id="b2022-108">Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="b2022-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="b2022-109">Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="b2022-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2022-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2022-110">Remarks</span></span>

<span data-ttu-id="b2022-111">Esse atributo é usado com o método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b2022-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2022-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2022-112">Requirements</span></span>



| <span data-ttu-id="b2022-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2022-113">Requirement</span></span> | <span data-ttu-id="b2022-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b2022-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2022-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2022-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b2022-116">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b2022-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="b2022-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2022-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b2022-118">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b2022-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="b2022-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2022-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2022-120"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2022-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2022-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2022-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2022-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b2022-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




