---
description: Especifica para uma topologia de transcodificação se o carregador de topologia carregar transformações baseadas em hardware.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: Atributo MF_TRANSCODE_TOPOLOGYMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827415"
---
# <a name="mf_transcode_topologymode-attribute"></a><span data-ttu-id="f57a2-103">\_Atributo topologymode de transcodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="f57a2-103">MF\_TRANSCODE\_TOPOLOGYMODE attribute</span></span>

<span data-ttu-id="f57a2-104">Especifica para uma topologia de transcodificação se o carregador de topologia carregar transformações baseadas em hardware.</span><span class="sxs-lookup"><span data-stu-id="f57a2-104">Specifies for a transcode topology whether the topology loader will load hardware-based transforms.</span></span>

<span data-ttu-id="f57a2-105">O modo de topologia especifica se as transformações de hardware (como codecs de hardware) podem ser usadas na topologia de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="f57a2-105">The topology mode specifies whether hardware transforms (such as hardware codecs) may be used in the transcode topology.</span></span> <span data-ttu-id="f57a2-106">O aplicativo pode armazenar esse atributo em um perfil de transcodificação chamando [**IMFTranscodeProfile:: Setcontêinerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span><span class="sxs-lookup"><span data-stu-id="f57a2-106">The application can store this attribute in a transcode profile by calling [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span>

## <a name="data-type"></a><span data-ttu-id="f57a2-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f57a2-107">Data type</span></span>

<span data-ttu-id="f57a2-108">**[**MF \_ Transcodificar \_ \_ sinalizadores topologymode**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** armazenados como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="f57a2-108">**[**MF\_TRANSCODE\_TOPOLOGYMODE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f57a2-109">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="f57a2-109">Get/set</span></span>

<span data-ttu-id="f57a2-110">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f57a2-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f57a2-111">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f57a2-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f57a2-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f57a2-112">Remarks</span></span>

<span data-ttu-id="f57a2-113">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="f57a2-113">This attribute is optional.</span></span> <span data-ttu-id="f57a2-114">Ele deve ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f57a2-114">It must have one of the following values.</span></span>



| <span data-ttu-id="f57a2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f57a2-115">Value</span></span>                                              | <span data-ttu-id="f57a2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f57a2-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f57a2-117">**HARDWARE do MF \_ transcodificar \_ topologymode \_ \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="f57a2-117">**MF\_TRANSCODE\_TOPOLOGYMODE\_HARDWARE\_ALLOWED**</span></span> | <span data-ttu-id="f57a2-118">O carregador de topologia carregará MFTs baseadas em hardware, como decodificadores de hardware, quando disponível.</span><span class="sxs-lookup"><span data-stu-id="f57a2-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="f57a2-119">O carregador de topologia voltará automaticamente para a decodificação de software se nenhum decodificador de hardware for encontrado ou se um decodificador de hardware não conseguir se conectar por algum motivo.</span><span class="sxs-lookup"><span data-stu-id="f57a2-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="f57a2-120">**\_somente software MF transcodificar \_ topologymode \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f57a2-120">**MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**</span></span>    | <span data-ttu-id="f57a2-121">O carregador de topologia carregará apenas MFTs de software, incluindo os decodificadores de software.</span><span class="sxs-lookup"><span data-stu-id="f57a2-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="f57a2-122">O valor padrão é **MF \_ transcodificar \_ topologymode \_ \_ somente software**.</span><span class="sxs-lookup"><span data-stu-id="f57a2-122">The default value is **MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**.</span></span>

<span data-ttu-id="f57a2-123">Se o carregador de topologia inserir uma MFT de hardware na topologia, ele definirá o atributo de atributo de URL de hardware de enumeração de MFT no nó de topologia. [ \_ \_ \_ \_ ](mft-enum-hardware-url-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="f57a2-123">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="f57a2-124">Para verificar se um MFT de hardware está presente, enumere os nós na topologia resolvida e verifique se esse atributo está presente.</span><span class="sxs-lookup"><span data-stu-id="f57a2-124">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="f57a2-125">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f57a2-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f57a2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f57a2-126">Requirements</span></span>



| <span data-ttu-id="f57a2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f57a2-127">Requirement</span></span> | <span data-ttu-id="f57a2-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f57a2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f57a2-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f57a2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f57a2-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f57a2-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f57a2-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f57a2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f57a2-132">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f57a2-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f57a2-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f57a2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f57a2-134"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f57a2-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f57a2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f57a2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f57a2-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f57a2-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f57a2-137">API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="f57a2-137">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="f57a2-138">**IMFTranscodeProfile:: getcontainerattributes**</span><span class="sxs-lookup"><span data-stu-id="f57a2-138">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="f57a2-139">**IMFTranscodeProfile:: setcontainerattributes**</span><span class="sxs-lookup"><span data-stu-id="f57a2-139">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




