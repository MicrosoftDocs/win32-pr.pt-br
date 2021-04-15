---
description: Contém um ponteiro para a fonte de mídia associada a um nó de topologia.
ms.assetid: 73b84ab6-bdc2-4b22-9ce4-b79b954476e5
title: Atributo MF_TOPONODE_SOURCE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57904e9797e0f669b2cb782750e4ae9199059d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502112"
---
# <a name="mf_toponode_source-attribute"></a><span data-ttu-id="b92d7-103">\_Atributo de \_ origem MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="b92d7-103">MF\_TOPONODE\_SOURCE attribute</span></span>

<span data-ttu-id="b92d7-104">Contém um ponteiro para a fonte de mídia associada a um nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="b92d7-104">Contains a pointer to the media source associated with a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="b92d7-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b92d7-105">Data type</span></span>

<span data-ttu-id="b92d7-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="b92d7-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="b92d7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b92d7-107">Remarks</span></span>

<span data-ttu-id="b92d7-108">Esse atributo se aplica a nós de origem (_ \* SOURCESTREAM de topologia do MF \_ \_ \_ nó \* \*).</span><span class="sxs-lookup"><span data-stu-id="b92d7-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="b92d7-109">O valor do atributo é um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="b92d7-109">The value of the attribute is a pointer to the media source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="b92d7-110">Esse atributo é necessário.</span><span class="sxs-lookup"><span data-stu-id="b92d7-110">This attribute is required.</span></span>

<span data-ttu-id="b92d7-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b92d7-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b92d7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b92d7-112">Requirements</span></span>



| <span data-ttu-id="b92d7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b92d7-113">Requirement</span></span> | <span data-ttu-id="b92d7-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b92d7-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b92d7-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b92d7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b92d7-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b92d7-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b92d7-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b92d7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b92d7-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b92d7-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b92d7-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b92d7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b92d7-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b92d7-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b92d7-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b92d7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b92d7-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b92d7-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b92d7-123">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="b92d7-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="b92d7-124">**IMFAttributes:: setunknown**</span><span class="sxs-lookup"><span data-stu-id="b92d7-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="b92d7-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="b92d7-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b92d7-126">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="b92d7-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




