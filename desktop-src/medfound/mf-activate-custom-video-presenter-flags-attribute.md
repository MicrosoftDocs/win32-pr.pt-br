---
description: Especifica como criar um apresentador personalizado para o processador de vídeo avançado (EVR).
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: Atributo MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3681edaed39b63b0f7c13313039f1c6e72311a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011339"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a><span data-ttu-id="c6b2f-103">MF \_ Ativar \_ o \_ atributo de \_ sinalizadores do apresentador de vídeo personalizado \_</span><span class="sxs-lookup"><span data-stu-id="c6b2f-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_FLAGS attribute</span></span>

<span data-ttu-id="c6b2f-104">Especifica como criar um apresentador personalizado para o processador de vídeo avançado (EVR).</span><span class="sxs-lookup"><span data-stu-id="c6b2f-104">Specifies how to create a custom presenter for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="c6b2f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c6b2f-105">Data type</span></span>

<span data-ttu-id="c6b2f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c6b2f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c6b2f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6b2f-107">Remarks</span></span>

<span data-ttu-id="c6b2f-108">Você pode definir esse atributo no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) obtido da função [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="c6b2f-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="c6b2f-109">O valor desse atributo é **uma operação or** dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="c6b2f-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="c6b2f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="c6b2f-110">Value</span></span>                                          | <span data-ttu-id="c6b2f-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6b2f-111">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b2f-112">**MF \_ Ativar \_ \_ apresentador personalizado \_ ALLOWFAIL**</span><span class="sxs-lookup"><span data-stu-id="c6b2f-112">**MF\_ACTIVATE\_CUSTOM\_PRESENTER\_ALLOWFAIL**</span></span> | <span data-ttu-id="c6b2f-113">Se o método [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) falhar ao criar o apresentador personalizado do aplicativo, ele usará o apresentador EVR padrão em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c6b2f-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom presenter, it uses the default EVR presenter instead.</span></span> <span data-ttu-id="c6b2f-114">Por padrão, se o objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) falhar ao tentar criar o apresentador personalizado, o método **activateobject** falhará.</span><span class="sxs-lookup"><span data-stu-id="c6b2f-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom presenter, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="c6b2f-115">Os aplicativos podem usar o atributo do [**\_ \_ \_ \_ \_ CLSID ativar vídeo personalizado do MF**](mf-activate-custom-video-presenter-clsid-attribute.md) para especificar um apresentador personalizado para o EVR.</span><span class="sxs-lookup"><span data-stu-id="c6b2f-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md) attribute to specify a custom presenter for the EVR.</span></span>

<span data-ttu-id="c6b2f-116">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c6b2f-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b2f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6b2f-117">Requirements</span></span>



| <span data-ttu-id="c6b2f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6b2f-118">Requirement</span></span> | <span data-ttu-id="c6b2f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c6b2f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b2f-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6b2f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b2f-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6b2f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c6b2f-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6b2f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b2f-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6b2f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c6b2f-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6b2f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6b2f-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6b2f-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6b2f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6b2f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6b2f-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6b2f-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6b2f-128">Atributos avançados de processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="c6b2f-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6b2f-129">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c6b2f-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c6b2f-130">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="c6b2f-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c6b2f-131">Objetos de ativação</span><span class="sxs-lookup"><span data-stu-id="c6b2f-131">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="c6b2f-132">Como escrever um apresentador EVR</span><span class="sxs-lookup"><span data-stu-id="c6b2f-132">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




