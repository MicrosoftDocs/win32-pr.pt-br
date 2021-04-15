---
description: Especifica se a transformação associada a um nó de topologia dá suporte a DXVA (aceleração de vídeo do DirectX).
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: Atributo MF_TOPONODE_D3DAWARE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461332"
---
# <a name="mf_toponode_d3daware-attribute"></a><span data-ttu-id="90a1f-103">\_Atributo MF TOPONODE \_ D3DAWARE</span><span class="sxs-lookup"><span data-stu-id="90a1f-103">MF\_TOPONODE\_D3DAWARE attribute</span></span>

<span data-ttu-id="90a1f-104">Especifica se a transformação associada a um nó de topologia dá suporte a DXVA (aceleração de vídeo do DirectX).</span><span class="sxs-lookup"><span data-stu-id="90a1f-104">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA).</span></span>

## <a name="data-type"></a><span data-ttu-id="90a1f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="90a1f-105">Data type</span></span>

<span data-ttu-id="90a1f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="90a1f-106">**UINT32**</span></span>

<span data-ttu-id="90a1f-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="90a1f-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90a1f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="90a1f-108">Remarks</span></span>

<span data-ttu-id="90a1f-109">Esse atributo se aplica a nós de transformação (**\_ nó de \_ transformação \_ de topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="90a1f-109">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="90a1f-110">Normalmente, os aplicativos não usam esse atributo diretamente.</span><span class="sxs-lookup"><span data-stu-id="90a1f-110">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="90a1f-111">A sessão de mídia define esse atributo em um nó de transformação se a transformação de Media Foundation subjacente tiver o atributo de [**\_ \_ \_ reconhecimento de D3D SA do MF**](mf-sa-d3d-aware-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="90a1f-111">The Media Session sets this attribute on a transform node if the underlying Media Foundation transform has the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute.</span></span>

<span data-ttu-id="90a1f-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="90a1f-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="90a1f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90a1f-113">Requirements</span></span>



| <span data-ttu-id="90a1f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="90a1f-114">Requirement</span></span> | <span data-ttu-id="90a1f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="90a1f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90a1f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90a1f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="90a1f-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90a1f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="90a1f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90a1f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="90a1f-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="90a1f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="90a1f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90a1f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="90a1f-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90a1f-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90a1f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="90a1f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a1f-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90a1f-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="90a1f-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="90a1f-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="90a1f-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="90a1f-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="90a1f-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="90a1f-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="90a1f-127">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="90a1f-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




