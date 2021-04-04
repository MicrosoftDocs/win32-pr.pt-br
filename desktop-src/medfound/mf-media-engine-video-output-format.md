---
description: Define o formato de destino de renderização para o mecanismo de mídia.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: Atributo MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663784"
---
# <a name="mf_media_engine_video_output_format-attribute"></a><span data-ttu-id="80a29-103">\_Atributo de \_ \_ formato de saída de vídeo do mecanismo de \_ mídia MF \_</span><span class="sxs-lookup"><span data-stu-id="80a29-103">MF\_MEDIA\_ENGINE\_VIDEO\_OUTPUT\_FORMAT attribute</span></span>

<span data-ttu-id="80a29-104">Define o formato de destino de renderização para o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="80a29-104">Sets the render-target format for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="80a29-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="80a29-105">Data type</span></span>

<span data-ttu-id="80a29-106">**Dxgi \_ FORMATO** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="80a29-106">**DXGI\_FORMAT** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="80a29-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="80a29-107">Remarks</span></span>

<span data-ttu-id="80a29-108">Defina esse atributo se você criar o mecanismo de mídia no modo de servidor de quadro.</span><span class="sxs-lookup"><span data-stu-id="80a29-108">Set this attribute if you create the Media Engine in frame-server mode.</span></span> <span data-ttu-id="80a29-109">Para obter mais informações, consulte [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="80a29-109">For more information, see [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="80a29-110">O valor do atributo é um valor [de \_ formato dxgi](../direct3d9/d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="80a29-110">The value of the attribute is a [DXGI\_FORMAT](../direct3d9/d3dformat.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="80a29-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80a29-111">Requirements</span></span>



| <span data-ttu-id="80a29-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="80a29-112">Requirement</span></span> | <span data-ttu-id="80a29-113">Valor</span><span class="sxs-lookup"><span data-stu-id="80a29-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="80a29-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80a29-114">Minimum supported client</span></span><br/> | <span data-ttu-id="80a29-115">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="80a29-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="80a29-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80a29-116">Minimum supported server</span></span><br/> | <span data-ttu-id="80a29-117">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="80a29-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="80a29-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80a29-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="80a29-119"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="80a29-119"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80a29-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="80a29-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a29-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80a29-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
