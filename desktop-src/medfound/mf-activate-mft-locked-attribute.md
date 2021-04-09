---
description: Especifica se o carregador de topologia alterará os tipos de mídia em uma Media Foundation transformação (MFT). Normalmente, os aplicativos não usam esse atributo.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: Atributo MF_ACTIVATE_MFT_LOCKED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d6dcb6cb60f760d87761a18b2b83545937878c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091159"
---
# <a name="mf_activate_mft_locked-attribute"></a><span data-ttu-id="d7625-104">MF \_ Ativar \_ atributo do MFT \_ bloqueado</span><span class="sxs-lookup"><span data-stu-id="d7625-104">MF\_ACTIVATE\_MFT\_LOCKED attribute</span></span>

<span data-ttu-id="d7625-105">Especifica se o carregador de topologia alterará os tipos de mídia em uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="d7625-105">Specifies whether the Topology Loader will change the media types on a Media Foundation transform (MFT).</span></span> <span data-ttu-id="d7625-106">Normalmente, os aplicativos não usam esse atributo.</span><span class="sxs-lookup"><span data-stu-id="d7625-106">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="d7625-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d7625-107">Data type</span></span>

<span data-ttu-id="d7625-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d7625-108">**UINT32**</span></span>

<span data-ttu-id="d7625-109">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="d7625-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7625-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7625-110">Remarks</span></span>

<span data-ttu-id="d7625-111">Se o valor desse atributo for diferente de zero, o carregador de topologia não alterará os tipos de mídia no MFT.</span><span class="sxs-lookup"><span data-stu-id="d7625-111">If value of this attribute is nonzero, the topology loader will not change the media types on the MFT.</span></span> <span data-ttu-id="d7625-112">O carregador de topologia define esse atributo depois de carregar a topologia.</span><span class="sxs-lookup"><span data-stu-id="d7625-112">The topology loader sets this attribute after it loads the topology.</span></span>

<span data-ttu-id="d7625-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d7625-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7625-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7625-114">Requirements</span></span>



| <span data-ttu-id="d7625-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7625-115">Requirement</span></span> | <span data-ttu-id="d7625-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d7625-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7625-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7625-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d7625-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7625-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d7625-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7625-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d7625-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d7625-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d7625-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7625-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7625-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7625-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7625-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7625-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7625-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7625-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7625-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d7625-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d7625-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="d7625-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d7625-127">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="d7625-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




