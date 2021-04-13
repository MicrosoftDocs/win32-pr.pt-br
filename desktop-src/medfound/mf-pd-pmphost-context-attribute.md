---
description: Contém um ponteiro para o objeto proxy para o descritor de apresentação de aplicativos.
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: Atributo MF_PD_PMPHOST_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370743"
---
# <a name="mf_pd_pmphost_context-attribute"></a><span data-ttu-id="df6d7-103">\_Atributo de contexto MF PD \_ PMPHOST \_</span><span class="sxs-lookup"><span data-stu-id="df6d7-103">MF\_PD\_PMPHOST\_CONTEXT attribute</span></span>

<span data-ttu-id="df6d7-104">Contém um ponteiro para o objeto proxy para o descritor de apresentação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="df6d7-104">Contains a pointer to the proxy object for the application's presentation descriptor.</span></span>

## <a name="data-type"></a><span data-ttu-id="df6d7-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="df6d7-105">Data type</span></span>

<span data-ttu-id="df6d7-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="df6d7-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="df6d7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="df6d7-107">Remarks</span></span>

<span data-ttu-id="df6d7-108">O host do caminho de mídia protegido (PMP) usa esse atributo para armazenar o descritor de apresentação do aplicativo no descritor de apresentação remoto.</span><span class="sxs-lookup"><span data-stu-id="df6d7-108">The Protected Media Path (PMP) host uses this attribute to store the application's presentation descriptor on the remote presentation descriptor.</span></span> <span data-ttu-id="df6d7-109">O valor do atributo é um ponteiro para a interface [_ *IMFRemoteProxy* \*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) .</span><span class="sxs-lookup"><span data-stu-id="df6d7-109">The attribute value is a pointer to the [_ *IMFRemoteProxy*\*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) interface.</span></span>

<span data-ttu-id="df6d7-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="df6d7-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="df6d7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df6d7-111">Requirements</span></span>



| <span data-ttu-id="df6d7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="df6d7-112">Requirement</span></span> | <span data-ttu-id="df6d7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="df6d7-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="df6d7-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df6d7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="df6d7-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df6d7-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="df6d7-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df6d7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="df6d7-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df6d7-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="df6d7-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df6d7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="df6d7-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="df6d7-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df6d7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="df6d7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6d7-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="df6d7-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="df6d7-122">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="df6d7-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="df6d7-123">**IMFAttributes:: setunknown**</span><span class="sxs-lookup"><span data-stu-id="df6d7-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="df6d7-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="df6d7-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="df6d7-125">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="df6d7-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




