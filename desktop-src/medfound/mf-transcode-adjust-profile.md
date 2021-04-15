---
description: Sinalizadores de perfil que definem as configurações de fluxo para a topologia de transcodificação. Os sinalizadores são definidos na enumeração MF \_ transcodificar \_ \_ sinalizadores de perfil \_ .
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: Atributo MF_TRANSCODE_ADJUST_PROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761427"
---
# <a name="mf_transcode_adjust_profile-attribute"></a><span data-ttu-id="b6a58-104">\_Atributo de \_ perfil de ajuste de TRANScodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="b6a58-104">MF\_TRANSCODE\_ADJUST\_PROFILE attribute</span></span>

<span data-ttu-id="b6a58-105">Sinalizadores de perfil que definem as configurações de fluxo para a topologia de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="b6a58-105">Profile flags that define the stream settings for the transcode topology.</span></span> <span data-ttu-id="b6a58-106">Os sinalizadores são definidos na enumeração [**MF \_ transcodificar \_ \_ \_ sinalizadores de perfil**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) .</span><span class="sxs-lookup"><span data-stu-id="b6a58-106">The flags are defined in the [**MF\_TRANSCODE\_ADJUST\_PROFILE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="b6a58-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b6a58-107">Data type</span></span>

<span data-ttu-id="b6a58-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b6a58-108">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b6a58-109">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="b6a58-109">Get/set</span></span>

<span data-ttu-id="b6a58-110">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b6a58-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b6a58-111">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b6a58-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6a58-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6a58-112">Remarks</span></span>

<span data-ttu-id="b6a58-113">Um aplicativo pode definir esse atributo no nível de contêiner no perfil transcodificar.</span><span class="sxs-lookup"><span data-stu-id="b6a58-113">An application can set this attribute at the container level on the transcode profile.</span></span> <span data-ttu-id="b6a58-114">Se esse atributo for definido, a função [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) alterará os atributos de fluxo durante a compilação da topologia, dependendo do sinalizador especificado.</span><span class="sxs-lookup"><span data-stu-id="b6a58-114">If this attribute is set, the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function changes the stream attributes during topology building, depending on the specified flag.</span></span> <span data-ttu-id="b6a58-115">Por exemplo, se o aplicativo especificar o **sinalizador \_ \_ padrão do \_ perfil \_ de ajuste de transcodificação MF** , as configurações de fluxo especificadas pelo aplicativo serão usadas para criar o perfil.</span><span class="sxs-lookup"><span data-stu-id="b6a58-115">For example, if the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_DEFAULT** flag, the application-specified stream settings are used to create the profile.</span></span>

<span data-ttu-id="b6a58-116">Para o fluxo de vídeo, a taxa de quadros é atualizada com base na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="b6a58-116">For the video stream, the frame rate is updated based on the media source.</span></span> <span data-ttu-id="b6a58-117">Se o aplicativo não especificar o modo entrelaçado, o perfil será atualizado para usar quadros progressivos por padrão.</span><span class="sxs-lookup"><span data-stu-id="b6a58-117">If the application does not specify the interlaced mode, the profile is updated to use progressive frames by default.</span></span>

<span data-ttu-id="b6a58-118">Se o aplicativo especificar o sinalizador de **\_ uso de \_ \_ \_ \_ \_ atributos de origem MF transcodificar** , os atributos de fluxo ausentes serão copiados da origem de mídia de entrada para as configurações de fluxo no perfil transcodificar.</span><span class="sxs-lookup"><span data-stu-id="b6a58-118">If the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_USE\_SOURCE\_ATTRIBUTES** flag, then missing stream attributes are copied from the input media source to the stream settings in the transcode profile.</span></span>

<span data-ttu-id="b6a58-119">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b6a58-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a58-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6a58-120">Requirements</span></span>



| <span data-ttu-id="b6a58-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6a58-121">Requirement</span></span> | <span data-ttu-id="b6a58-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b6a58-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a58-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6a58-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b6a58-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b6a58-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b6a58-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6a58-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b6a58-126">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="b6a58-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b6a58-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6a58-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6a58-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6a58-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6a58-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6a58-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6a58-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6a58-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b6a58-131">API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="b6a58-131">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="b6a58-132">**IMFTranscodeProfile:: setcontainerattributes**</span><span class="sxs-lookup"><span data-stu-id="b6a58-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




