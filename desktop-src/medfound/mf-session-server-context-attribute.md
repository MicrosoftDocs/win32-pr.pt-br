---
description: Permite que duas instâncias da sessão de mídia compartilhem o mesmo processo PMP (caminho de mídia protegido).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: Atributo MF_SESSION_SERVER_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ce68d1dcd4318f68c4547845e6ce12d2f3aaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091775"
---
# <a name="mf_session_server_context-attribute"></a><span data-ttu-id="cf804-103">\_Atributo de \_ contexto de servidor de sessão MF \_</span><span class="sxs-lookup"><span data-stu-id="cf804-103">MF\_SESSION\_SERVER\_CONTEXT attribute</span></span>

<span data-ttu-id="cf804-104">Permite que duas instâncias da sessão de mídia compartilhem o mesmo processo PMP (caminho de mídia protegido).</span><span class="sxs-lookup"><span data-stu-id="cf804-104">Enables two instances of the Media Session to share the same Protected Media Path (PMP) process.</span></span>

## <a name="data-type"></a><span data-ttu-id="cf804-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cf804-105">Data type</span></span>

<span data-ttu-id="cf804-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="cf804-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="cf804-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf804-107">Remarks</span></span>

<span data-ttu-id="cf804-108">Use esse atributo se você quiser criar a sessão de mídia do PMP em um processo de PMP existente.</span><span class="sxs-lookup"><span data-stu-id="cf804-108">Use this attribute if you want to create the PMP Media Session in an existing PMP process.</span></span> <span data-ttu-id="cf804-109">O valor do atributo é um ponteiro para a interface [_ *IMFPMPServer* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) .</span><span class="sxs-lookup"><span data-stu-id="cf804-109">The value of the attribute is a pointer to the [_ *IMFPMPServer*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) interface.</span></span>

<span data-ttu-id="cf804-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="cf804-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf804-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf804-111">Requirements</span></span>



| <span data-ttu-id="cf804-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf804-112">Requirement</span></span> | <span data-ttu-id="cf804-113">Valor</span><span class="sxs-lookup"><span data-stu-id="cf804-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf804-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf804-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cf804-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf804-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cf804-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf804-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cf804-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf804-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cf804-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf804-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf804-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf804-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf804-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf804-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf804-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cf804-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cf804-122">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="cf804-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="cf804-123">**IMFAttributes:: setunknown**</span><span class="sxs-lookup"><span data-stu-id="cf804-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="cf804-124">Atributos de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="cf804-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




