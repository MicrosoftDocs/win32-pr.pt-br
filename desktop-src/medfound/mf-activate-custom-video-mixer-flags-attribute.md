---
description: Especifica como criar um mixer personalizado para o processador de vídeo avançado (EVR).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: Atributo MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b17a0063b7ef4b6a1cbb5993ea2fb7af2a4a678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662611"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a><span data-ttu-id="8ab0b-103">MF \_ Ativar \_ \_ atributo de \_ sinalizadores de mixer de vídeo personalizado \_</span><span class="sxs-lookup"><span data-stu-id="8ab0b-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_FLAGS attribute</span></span>

<span data-ttu-id="8ab0b-104">Especifica como criar um mixer personalizado para o processador de vídeo avançado (EVR).</span><span class="sxs-lookup"><span data-stu-id="8ab0b-104">Specifies how to create a custom mixer for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="8ab0b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8ab0b-105">Data type</span></span>

<span data-ttu-id="8ab0b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8ab0b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8ab0b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ab0b-107">Remarks</span></span>

<span data-ttu-id="8ab0b-108">Você pode definir esse atributo no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) obtido da função [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="8ab0b-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="8ab0b-109">O valor desse atributo é **uma operação or** dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="8ab0b-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="8ab0b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="8ab0b-110">Value</span></span>                                      | <span data-ttu-id="8ab0b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ab0b-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ab0b-112">**MF \_ Ativar \_ \_ mixer personalizado \_ ALLOWFAIL**</span><span class="sxs-lookup"><span data-stu-id="8ab0b-112">**MF\_ACTIVATE\_CUSTOM\_MIXER\_ALLOWFAIL**</span></span> | <span data-ttu-id="8ab0b-113">Se o método [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) falhar ao criar o mixer personalizado do aplicativo, ele usará o mixer EVR padrão em vez disso.</span><span class="sxs-lookup"><span data-stu-id="8ab0b-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom mixer, it uses the default EVR mixer instead.</span></span> <span data-ttu-id="8ab0b-114">Por padrão, se o objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) falhar ao tentar criar o mixer personalizado, o método **activateobject** falhará.</span><span class="sxs-lookup"><span data-stu-id="8ab0b-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom mixer, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="8ab0b-115">Os aplicativos podem usar o atributo de [**\_ \_ \_ CLSID ativar \_ mixer \_ de vídeo personalizado MF**](mf-activate-custom-video-mixer-clsid-attribute.md) para especificar um mixer personalizado para o EVR.</span><span class="sxs-lookup"><span data-stu-id="8ab0b-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md) attribute to specify a custom mixer for the EVR.</span></span>

<span data-ttu-id="8ab0b-116">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8ab0b-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ab0b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ab0b-117">Requirements</span></span>



| <span data-ttu-id="8ab0b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ab0b-118">Requirement</span></span> | <span data-ttu-id="8ab0b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8ab0b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ab0b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ab0b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8ab0b-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ab0b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8ab0b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ab0b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8ab0b-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ab0b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8ab0b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ab0b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ab0b-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ab0b-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ab0b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ab0b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ab0b-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8ab0b-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8ab0b-128">Atributos avançados de processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="8ab0b-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="8ab0b-129">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8ab0b-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8ab0b-130">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="8ab0b-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8ab0b-131">Objetos de ativação</span><span class="sxs-lookup"><span data-stu-id="8ab0b-131">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




