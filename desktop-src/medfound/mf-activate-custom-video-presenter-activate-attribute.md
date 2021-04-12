---
description: Especifica um objeto de ativação que cria um apresentador de vídeo personalizado para o coletor de mídia do EVR (processador de vídeo avançado).
ms.assetid: 65d88832-0969-4d85-bee2-fd0aa68e9f3b
title: Atributo MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75855c18faba8568547f9efcfb19e04574c4885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296570"
---
# <a name="mf_activate_custom_video_presenter_activate-attribute"></a><span data-ttu-id="452c4-103">Ativar \_ \_ atributo do \_ \_ apresentador de vídeo personalizado \_ MF ativar</span><span class="sxs-lookup"><span data-stu-id="452c4-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_ACTIVATE attribute</span></span>

<span data-ttu-id="452c4-104">Especifica um objeto de ativação que cria um apresentador de vídeo personalizado para o coletor de mídia do EVR (processador de vídeo avançado).</span><span class="sxs-lookup"><span data-stu-id="452c4-104">Specifies an activation object that creates a custom video presenter for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="452c4-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="452c4-105">Data type</span></span>

<span data-ttu-id="452c4-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="452c4-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="452c4-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="452c4-107">Remarks</span></span>

<span data-ttu-id="452c4-108">Se você estiver criando o EVR por meio de um objeto de ativação, poderá usar esse atributo para definir um apresentador de vídeo personalizado no EVR.</span><span class="sxs-lookup"><span data-stu-id="452c4-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video presenter on the EVR.</span></span> <span data-ttu-id="452c4-109">Use este atributo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="452c4-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="452c4-110">Chame a função [_ *MFCreateVideoRendererActivate* \*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar um objeto de ativação para o EVR.</span><span class="sxs-lookup"><span data-stu-id="452c4-110">Call the [_ *MFCreateVideoRendererActivate*\*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="452c4-111">A função retorna um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="452c4-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="452c4-112">Defina esse atributo no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chamando [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="452c4-112">Set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span> <span data-ttu-id="452c4-113">O valor do atributo é um ponteiro para um objeto de ativação implementado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="452c4-113">The value of the attribute is a pointer to an activation object implemented by the caller.</span></span> <span data-ttu-id="452c4-114">O objeto de ativação do chamador deve expor a interface **IMFActivate** .</span><span class="sxs-lookup"><span data-stu-id="452c4-114">The caller's activation object must expose the **IMFActivate** interface.</span></span>

<span data-ttu-id="452c4-115">Se você definir esse atributo, o EVR chamará [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para criar o apresentador de vídeo personalizado.</span><span class="sxs-lookup"><span data-stu-id="452c4-115">If you set this attribute, the EVR calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the custom video presenter.</span></span> <span data-ttu-id="452c4-116">O apresentador de vídeo deve expor a interface [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) .</span><span class="sxs-lookup"><span data-stu-id="452c4-116">The video presenter must expose the [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface.</span></span>

<span data-ttu-id="452c4-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="452c4-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="452c4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="452c4-118">Requirements</span></span>



| <span data-ttu-id="452c4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="452c4-119">Requirement</span></span> | <span data-ttu-id="452c4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="452c4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="452c4-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="452c4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="452c4-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="452c4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="452c4-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="452c4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="452c4-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="452c4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="452c4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="452c4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="452c4-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="452c4-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="452c4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="452c4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="452c4-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="452c4-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="452c4-129">Atributos avançados de processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="452c4-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="452c4-130">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="452c4-130">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="452c4-131">**IMFAttributes:: setunknown**</span><span class="sxs-lookup"><span data-stu-id="452c4-131">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="452c4-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="452c4-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="452c4-133">Objetos de ativação</span><span class="sxs-lookup"><span data-stu-id="452c4-133">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="452c4-134">Como escrever um apresentador EVR</span><span class="sxs-lookup"><span data-stu-id="452c4-134">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




