---
description: Contém um ponteiro para o descritor de apresentação para a origem da mídia.
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: Atributo MF_TOPONODE_PRESENTATION_DESCRIPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d95fae4f2c4d4a482c2a62d57e0835ea4f1c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647564"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a><span data-ttu-id="c87ca-103">\_Atributo de \_ descritor de apresentação TOPONODE MF \_</span><span class="sxs-lookup"><span data-stu-id="c87ca-103">MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="c87ca-104">Contém um ponteiro para o descritor de apresentação para a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="c87ca-104">Contains a pointer to the presentation descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="c87ca-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c87ca-105">Data type</span></span>

<span data-ttu-id="c87ca-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="c87ca-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="c87ca-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c87ca-107">Remarks</span></span>

<span data-ttu-id="c87ca-108">Esse atributo se aplica a nós de origem (_ \* SOURCESTREAM de topologia do MF \_ \_ \_ nó \* \*).</span><span class="sxs-lookup"><span data-stu-id="c87ca-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="c87ca-109">O valor do atributo é um ponteiro para a interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) do descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="c87ca-109">The value of the attribute is a pointer to the presentation descriptor's [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span> <span data-ttu-id="c87ca-110">Esse atributo é necessário.</span><span class="sxs-lookup"><span data-stu-id="c87ca-110">This attribute is required.</span></span>

<span data-ttu-id="c87ca-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c87ca-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c87ca-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c87ca-112">Requirements</span></span>



| <span data-ttu-id="c87ca-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c87ca-113">Requirement</span></span> | <span data-ttu-id="c87ca-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c87ca-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c87ca-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c87ca-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c87ca-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c87ca-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c87ca-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c87ca-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c87ca-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c87ca-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c87ca-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c87ca-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c87ca-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c87ca-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c87ca-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c87ca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c87ca-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c87ca-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c87ca-123">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="c87ca-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="c87ca-124">**IMFAttributes:: setunknown**</span><span class="sxs-lookup"><span data-stu-id="c87ca-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="c87ca-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="c87ca-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="c87ca-126">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c87ca-126">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




