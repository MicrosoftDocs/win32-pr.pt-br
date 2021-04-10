---
description: Contém o idioma preferencial RFC 1766 da fonte de mídia.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: Atributo MF_PD_PREFERRED_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bb121c7181724ef06b3e8fe9239342a140104a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171730"
---
# <a name="mf_pd_preferred_language-attribute"></a><span data-ttu-id="12c98-103">\_Atributo de \_ \_ idioma preferencial do MF PD</span><span class="sxs-lookup"><span data-stu-id="12c98-103">MF\_PD\_PREFERRED\_LANGUAGE attribute</span></span>

<span data-ttu-id="12c98-104">Contém o idioma preferencial RFC 1766 da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="12c98-104">Contains the preferred RFC 1766 language of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="12c98-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="12c98-105">Data type</span></span>

<span data-ttu-id="12c98-106">**WCHAR**</span><span class="sxs-lookup"><span data-stu-id="12c98-106">**WCHAR**</span></span>

## <a name="getset"></a><span data-ttu-id="12c98-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="12c98-107">Get/set</span></span>

<span data-ttu-id="12c98-108">Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="12c98-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="12c98-109">Para definir esse atributo, chame [**IMFAttributes:: setastring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="12c98-109">To set this attribute, call [**IMFAttributes::Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="12c98-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="12c98-110">Applies to</span></span>

[<span data-ttu-id="12c98-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="12c98-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="12c98-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="12c98-112">Remarks</span></span>

<span data-ttu-id="12c98-113">O \_ atributo de linguagem MF PD \_ preferencial \_ é opcional.</span><span class="sxs-lookup"><span data-stu-id="12c98-113">The MF\_PD\_PREFERRED\_LANGUAGE attribute is optional.</span></span> <span data-ttu-id="12c98-114">Um aplicativo pode definir esse atributo em uma fonte de mídia (como uma fonte de rede) para especificar seu idioma preferencial.</span><span class="sxs-lookup"><span data-stu-id="12c98-114">An application can set this attribute on a media source (such as a network source) to specify its preferred language.</span></span>

<span data-ttu-id="12c98-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="12c98-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="12c98-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12c98-116">Requirements</span></span>



| <span data-ttu-id="12c98-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="12c98-117">Requirement</span></span> | <span data-ttu-id="12c98-118">Valor</span><span class="sxs-lookup"><span data-stu-id="12c98-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="12c98-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12c98-119">Minimum supported client</span></span><br/> | <span data-ttu-id="12c98-120">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="12c98-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="12c98-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12c98-121">Minimum supported server</span></span><br/> | <span data-ttu-id="12c98-122">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="12c98-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="12c98-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12c98-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="12c98-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12c98-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12c98-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="12c98-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c98-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12c98-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="12c98-127">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="12c98-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




