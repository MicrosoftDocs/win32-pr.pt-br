---
description: CLSID de um apresentador de vídeo personalizado para o coletor de mídia do EVR (processador de vídeo avançado).
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: Atributo MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0eb913a56671d5d2ac8d27c785e1cc1fbfc51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781571"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a><span data-ttu-id="ad6f4-103">MF \_ Ativar \_ o \_ \_ atributo CLSID do apresentador de vídeo personalizado \_</span><span class="sxs-lookup"><span data-stu-id="ad6f4-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID attribute</span></span>

<span data-ttu-id="ad6f4-104">CLSID de um apresentador de vídeo personalizado para o coletor de mídia do EVR (processador de vídeo avançado).</span><span class="sxs-lookup"><span data-stu-id="ad6f4-104">CLSID of a custom video presenter for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad6f4-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad6f4-105">Data type</span></span>

<span data-ttu-id="ad6f4-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="ad6f4-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad6f4-107">Remarks</span></span>

<span data-ttu-id="ad6f4-108">Se você estiver criando o EVR por meio de um objeto de ativação, poderá usar esse atributo para definir um apresentador de vídeo personalizado no EVR.</span><span class="sxs-lookup"><span data-stu-id="ad6f4-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video presenter on the EVR.</span></span> <span data-ttu-id="ad6f4-109">Use este atributo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ad6f4-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="ad6f4-110">Chame a função [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar um objeto de ativação para o EVR.</span><span class="sxs-lookup"><span data-stu-id="ad6f4-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="ad6f4-111">A função retorna um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="ad6f4-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="ad6f4-112">Defina esse attribue no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chamando [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="ad6f4-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="ad6f4-113">O valor do atributo é o CLSID do apresentador de vídeo personalizado do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ad6f4-113">The value of the attribute is the CLSID of the application's custom video presenter.</span></span>

<span data-ttu-id="ad6f4-114">Se esse atributo for definido, o EVR chamará **CoCreateInstance** com o CLSID especificado para criar o apresentador de vídeo personalizado.</span><span class="sxs-lookup"><span data-stu-id="ad6f4-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video presenter.</span></span> <span data-ttu-id="ad6f4-115">O apresentador de vídeo deve expor a interface [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) .</span><span class="sxs-lookup"><span data-stu-id="ad6f4-115">The video presenter must expose the [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface.</span></span> <span data-ttu-id="ad6f4-116">O apresentador é criado como um servidor COM em processo.</span><span class="sxs-lookup"><span data-stu-id="ad6f4-116">The presenter is created as an in-process COM server.</span></span>

<span data-ttu-id="ad6f4-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ad6f4-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad6f4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad6f4-118">Requirements</span></span>



| <span data-ttu-id="ad6f4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad6f4-119">Requirement</span></span> | <span data-ttu-id="ad6f4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ad6f4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6f4-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad6f4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ad6f4-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ad6f4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ad6f4-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad6f4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ad6f4-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ad6f4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ad6f4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad6f4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad6f4-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad6f4-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad6f4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad6f4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad6f4-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad6f4-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad6f4-129">Atributos avançados de processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ad6f4-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad6f4-130">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="ad6f4-131">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="ad6f4-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="ad6f4-133">Objetos de ativação</span><span class="sxs-lookup"><span data-stu-id="ad6f4-133">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="ad6f4-134">Como escrever um apresentador EVR</span><span class="sxs-lookup"><span data-stu-id="ad6f4-134">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




