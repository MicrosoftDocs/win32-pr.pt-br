---
description: Contém um ponteiro para o descritor de fluxo para a origem da mídia.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: Atributo MF_TOPONODE_STREAM_DESCRIPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074a1c1ffde3671779362724676f884c3b6b0b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813687"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a><span data-ttu-id="0bcb9-103">\_Atributo de \_ descritor de fluxo TOPONODE MF \_</span><span class="sxs-lookup"><span data-stu-id="0bcb9-103">MF\_TOPONODE\_STREAM\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="0bcb9-104">Contém um ponteiro para o descritor de fluxo para a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-104">Contains a pointer to the stream descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="0bcb9-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0bcb9-105">Data type</span></span>

<span data-ttu-id="0bcb9-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="0bcb9-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="0bcb9-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bcb9-107">Remarks</span></span>

<span data-ttu-id="0bcb9-108">Esse atributo se aplica a nós de origem (_ \* SOURCESTREAM de topologia do MF \_ \_ \_ nó \* \*).</span><span class="sxs-lookup"><span data-stu-id="0bcb9-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="0bcb9-109">O valor do atributo é um ponteiro para a interface [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) do descritor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-109">The value of the attribute is a pointer to the stream descriptor's [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface.</span></span> <span data-ttu-id="0bcb9-110">Esse atributo é necessário.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-110">This attribute is required.</span></span>

<span data-ttu-id="0bcb9-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bcb9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bcb9-112">Requirements</span></span>



| <span data-ttu-id="0bcb9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bcb9-113">Requirement</span></span> | <span data-ttu-id="0bcb9-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0bcb9-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0bcb9-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bcb9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0bcb9-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0bcb9-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0bcb9-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bcb9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0bcb9-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0bcb9-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0bcb9-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0bcb9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bcb9-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bcb9-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bcb9-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bcb9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcb9-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0bcb9-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0bcb9-123">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="0bcb9-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="0bcb9-124">**IMFAttributes:: setunknown**</span><span class="sxs-lookup"><span data-stu-id="0bcb9-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="0bcb9-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="0bcb9-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="0bcb9-126">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="0bcb9-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




