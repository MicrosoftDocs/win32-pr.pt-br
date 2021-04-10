---
description: Especifica que a origem da mídia será criada em um processo remoto.
ms.assetid: 3a2f9ff5-1780-40f3-b36b-3a7cccb47d05
title: Atributo MF_SESSION_REMOTE_SOURCE_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27b26a71e8bea53ab687eaf6126a1803e71ba16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170513"
---
# <a name="mf_session_remote_source_mode-attribute"></a><span data-ttu-id="66a4f-103">\_Atributo do \_ \_ modo de origem remoto da sessão MF \_</span><span class="sxs-lookup"><span data-stu-id="66a4f-103">MF\_SESSION\_REMOTE\_SOURCE\_MODE attribute</span></span>

<span data-ttu-id="66a4f-104">Especifica que a origem da mídia será criada em um processo remoto.</span><span class="sxs-lookup"><span data-stu-id="66a4f-104">Specifies that the media source will be created in a remote process.</span></span>

## <a name="data-type"></a><span data-ttu-id="66a4f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="66a4f-105">Data type</span></span>

<span data-ttu-id="66a4f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="66a4f-106">**UINT32**</span></span>

<span data-ttu-id="66a4f-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="66a4f-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66a4f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="66a4f-108">Remarks</span></span>

<span data-ttu-id="66a4f-109">Você pode definir esse atributo na sessão do caminho de mídia protegida (PMP) usando o parâmetro *pConfiguration* da função [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="66a4f-109">You can set this attribute on the protected media path (PMP) session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="66a4f-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="66a4f-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="66a4f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66a4f-111">Requirements</span></span>



| <span data-ttu-id="66a4f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a4f-112">Requirement</span></span> | <span data-ttu-id="66a4f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="66a4f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66a4f-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66a4f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="66a4f-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66a4f-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66a4f-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66a4f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="66a4f-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66a4f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="66a4f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66a4f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="66a4f-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66a4f-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a4f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="66a4f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a4f-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66a4f-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66a4f-122">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="66a4f-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="66a4f-123">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="66a4f-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="66a4f-124">Atributos de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="66a4f-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="66a4f-125">Sessão de mídia do PMP</span><span class="sxs-lookup"><span data-stu-id="66a4f-125">PMP Media Session</span></span>](pmp-media-session.md)
</dt> </dl>

 

 




