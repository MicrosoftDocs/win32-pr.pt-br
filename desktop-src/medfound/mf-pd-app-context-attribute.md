---
description: Contém um ponteiro para o descritor de apresentação do caminho de mídia protegido (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: Atributo MF_PD_APP_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171029"
---
# <a name="mf_pd_app_context-attribute"></a><span data-ttu-id="b03cc-103">\_Atributo de \_ contexto de aplicativo MF PD \_</span><span class="sxs-lookup"><span data-stu-id="b03cc-103">MF\_PD\_APP\_CONTEXT attribute</span></span>

<span data-ttu-id="b03cc-104">Contém um ponteiro para o descritor de apresentação do caminho de mídia protegido (PMP).</span><span class="sxs-lookup"><span data-stu-id="b03cc-104">Contains a pointer to the presentation descriptor from the Protected Media Path (PMP).</span></span>

## <a name="data-type"></a><span data-ttu-id="b03cc-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b03cc-105">Data type</span></span>

<span data-ttu-id="b03cc-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="b03cc-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="b03cc-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b03cc-107">Remarks</span></span>

<span data-ttu-id="b03cc-108">O proxy de origem de mídia, que é criado no processo do PMP, usa esse atributo para armazenar o descritor de apresentação remoto no descritor de apresentação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b03cc-108">The media source proxy, which is created in the PMP process, uses this attribute to store the remote presentation descriptor on the application's presentation descriptor.</span></span>

<span data-ttu-id="b03cc-109">O valor desse atributo é um ponteiro para a interface [_ *IMFPresentationDescriptor* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="b03cc-109">The value of this attribute is a pointer to the [_ *IMFPresentationDescriptor*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span>

<span data-ttu-id="b03cc-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b03cc-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b03cc-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b03cc-111">Requirements</span></span>



| <span data-ttu-id="b03cc-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b03cc-112">Requirement</span></span> | <span data-ttu-id="b03cc-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b03cc-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b03cc-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b03cc-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b03cc-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b03cc-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b03cc-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b03cc-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b03cc-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b03cc-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b03cc-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b03cc-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b03cc-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b03cc-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b03cc-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b03cc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b03cc-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b03cc-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b03cc-122">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="b03cc-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="b03cc-123">**IMFAttributes:: setunknown**</span><span class="sxs-lookup"><span data-stu-id="b03cc-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="b03cc-124">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="b03cc-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




