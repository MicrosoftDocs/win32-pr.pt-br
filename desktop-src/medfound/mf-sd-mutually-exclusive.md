---
description: Especifica se um fluxo é mutuamente exclusivo com outros fluxos do mesmo tipo.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: Atributo MF_SD_MUTUALLY_EXCLUSIVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812041"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a><span data-ttu-id="0c5e9-103">\_Atributo de SD do MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="0c5e9-103">MF\_SD\_MUTUALLY\_EXCLUSIVE attribute</span></span>

<span data-ttu-id="0c5e9-104">Especifica se um fluxo é mutuamente exclusivo com outros fluxos do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="0c5e9-104">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span>

## <a name="data-type"></a><span data-ttu-id="0c5e9-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0c5e9-105">Data type</span></span>

<span data-ttu-id="0c5e9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0c5e9-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0c5e9-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="0c5e9-107">Get/set</span></span>

<span data-ttu-id="0c5e9-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0c5e9-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0c5e9-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0c5e9-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="0c5e9-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="0c5e9-110">Applies to</span></span>

[<span data-ttu-id="0c5e9-111">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0c5e9-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="0c5e9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c5e9-112">Remarks</span></span>

<span data-ttu-id="0c5e9-113">Se esse atributo for **true** (diferente de zero), o fluxo será mutuamente exclusivo com outros fluxos do mesmo tipo, como áudio ou vídeo, dentro da mesma apresentação.</span><span class="sxs-lookup"><span data-stu-id="0c5e9-113">If this attribute is **TRUE** (nonzero), the stream is mutually exclusive with other streams of the same type, such as audio or video, within the same presentation.</span></span> <span data-ttu-id="0c5e9-114">Por exemplo, se um arquivo AVI contiver vários fluxos de áudio, eles serão marcados como mutuamente exclusivos, porque apenas um fluxo de áudio deve ser reproduzido ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="0c5e9-114">For example, if an AVI file contains multiple audio streams, they are marked as mutually exclusive, because only one audio stream should be played at one time.</span></span>

<span data-ttu-id="0c5e9-115">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="0c5e9-115">The default value is **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="0c5e9-116">Esse atributo não é usado para arquivos ASF (Advanced Systems Format), que têm uma maneira mais sofisticada de representar critérios de exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="0c5e9-116">This attribute is not used for Advanced Systems Format (ASF) files, which have a more sophisticated way to represent mutual exclusion criteria.</span></span> <span data-ttu-id="0c5e9-117">Para obter mais informações, consulte [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="0c5e9-117">For more information, see [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span></span>

 

<span data-ttu-id="0c5e9-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0c5e9-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c5e9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c5e9-119">Requirements</span></span>



| <span data-ttu-id="0c5e9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c5e9-120">Requirement</span></span> | <span data-ttu-id="0c5e9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0c5e9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c5e9-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c5e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0c5e9-123">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0c5e9-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="0c5e9-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c5e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0c5e9-125">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="0c5e9-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0c5e9-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c5e9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c5e9-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c5e9-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c5e9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c5e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c5e9-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c5e9-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c5e9-130">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="0c5e9-130">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




