---
description: CLSID de um mixer de vídeo personalizado para o coletor de mídia EVR (processador de vídeo avançado).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: Atributo MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296438"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a><span data-ttu-id="a4b4c-103">MF \_ Ativar \_ o \_ \_ atributo CLSID do mixer de vídeo personalizado \_</span><span class="sxs-lookup"><span data-stu-id="a4b4c-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID attribute</span></span>

<span data-ttu-id="a4b4c-104">CLSID de um mixer de vídeo personalizado para o coletor de mídia EVR (processador de vídeo avançado).</span><span class="sxs-lookup"><span data-stu-id="a4b4c-104">CLSID of a custom video mixer for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="a4b4c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a4b4c-105">Data type</span></span>

<span data-ttu-id="a4b4c-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a4b4c-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b4c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4b4c-107">Remarks</span></span>

<span data-ttu-id="a4b4c-108">Se você estiver criando o EVR por meio de um objeto de ativação, poderá usar esse atributo para definir um mixer de vídeo personalizado no EVR.</span><span class="sxs-lookup"><span data-stu-id="a4b4c-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video mixer on the EVR.</span></span> <span data-ttu-id="a4b4c-109">Use este atributo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a4b4c-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="a4b4c-110">Chame a função [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar um objeto de ativação para o EVR.</span><span class="sxs-lookup"><span data-stu-id="a4b4c-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="a4b4c-111">A função retorna um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="a4b4c-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="a4b4c-112">Defina esse attribue no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chamando [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="a4b4c-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="a4b4c-113">O valor do atributo é o CLSID do mixer de vídeo personalizado do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a4b4c-113">The value of the attribute is the CLSID of the application's custom video mixer.</span></span>

<span data-ttu-id="a4b4c-114">Se esse atributo for definido, o EVR chamará **CoCreateInstance** com o CLSID especificado para criar o mixer de vídeo personalizado.</span><span class="sxs-lookup"><span data-stu-id="a4b4c-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video mixer.</span></span> <span data-ttu-id="a4b4c-115">O mixer de vídeo deve expor a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="a4b4c-115">The video mixer must expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="a4b4c-116">O Mixer é criado como um servidor COM em processo.</span><span class="sxs-lookup"><span data-stu-id="a4b4c-116">The mixer is created as an in-process COM server.</span></span>

<span data-ttu-id="a4b4c-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a4b4c-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b4c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4b4c-118">Requirements</span></span>



| <span data-ttu-id="a4b4c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4b4c-119">Requirement</span></span> | <span data-ttu-id="a4b4c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a4b4c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b4c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4b4c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b4c-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4b4c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a4b4c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4b4c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b4c-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4b4c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a4b4c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4b4c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4b4c-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b4c-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b4c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4b4c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b4c-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a4b4c-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a4b4c-129">Atributos avançados de processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4b4c-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="a4b4c-130">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="a4b4c-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="a4b4c-131">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="a4b4c-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="a4b4c-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="a4b4c-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="a4b4c-133">Objetos de ativação</span><span class="sxs-lookup"><span data-stu-id="a4b4c-133">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




