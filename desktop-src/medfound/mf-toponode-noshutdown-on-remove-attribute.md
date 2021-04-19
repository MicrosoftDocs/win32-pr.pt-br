---
description: Especifica como a sessão de mídia desliga um objeto na topologia.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: Atributo MF_TOPONODE_NOSHUTDOWN_ON_REMOVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786182"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a><span data-ttu-id="8ec5a-103">MF \_ TOPONODE \_ parashutdown \_ no \_ atributo remove</span><span class="sxs-lookup"><span data-stu-id="8ec5a-103">MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE attribute</span></span>

<span data-ttu-id="8ec5a-104">Especifica como a sessão de mídia desliga um objeto na topologia.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-104">Specifies how the Media Session shuts down an object in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="8ec5a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8ec5a-105">Data type</span></span>

<span data-ttu-id="8ec5a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8ec5a-106">**UINT32**</span></span>

<span data-ttu-id="8ec5a-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ec5a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ec5a-108">Remarks</span></span>

<span data-ttu-id="8ec5a-109">Esse atributo se aplica aos seguintes tipos de nó topologia:</span><span class="sxs-lookup"><span data-stu-id="8ec5a-109">This attribute applies to the following types of toplogy node:</span></span>

-   <span data-ttu-id="8ec5a-110">Nós de saída</span><span class="sxs-lookup"><span data-stu-id="8ec5a-110">Output nodes</span></span>
-   <span data-ttu-id="8ec5a-111">Qualquer nó de transformação que contenha uma Media Foundation de transformação *assíncrona* (MFT).</span><span class="sxs-lookup"><span data-stu-id="8ec5a-111">Any transform node that contains an *asynchronous* Media Foundation transform (MFT).</span></span>

<span data-ttu-id="8ec5a-112">O atributo pode ter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="8ec5a-112">The attribute can have the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ec5a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8ec5a-113">Value</span></span></th>
<th><span data-ttu-id="8ec5a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ec5a-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ec5a-115"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="8ec5a-115"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="8ec5a-116">Quando a sessão de mídia alterna para uma nova topologia ou limpa a topologia atual, ela não encerra o objeto que pertence a esse nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-116">When the Media Session switches to a new topology or clears the current topology, it does not shut down the object that belongs to this topology node.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ec5a-117"><strong>FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="8ec5a-117"><strong>FALSE</strong></span></span></td>
<td><span data-ttu-id="8ec5a-118">Quando a sessão de mídia alterna para uma nova topologia ou limpa a topologia atual, ela desliga o objeto de nó, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8ec5a-118">When the Media Session switches to a new topology or clears the current topology, it shuts down the node object, as follows:</span></span>
<ul>
<li><span data-ttu-id="8ec5a-119">Nós de saída: a sessão chama <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink:: Shutdown</strong></a> no coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-119">Output nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink::Shutdown</strong></a> on the media sink.</span></span></li>
<li><span data-ttu-id="8ec5a-120">Nós de transformação: a sessão chama <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown:: Shutdown</strong></a> no MFT.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-120">Transform nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown::Shutdown</strong></a> on the MFT.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8ec5a-121">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-121">The default value is **TRUE**.</span></span>

<span data-ttu-id="8ec5a-122">Se o seu aplicativo enfileira várias topologias, é uma boa ideia definir esse atributo como **false**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-122">If your application queues multiple topologies, it is a good idea to set this attribute to **FALSE**.</span></span> <span data-ttu-id="8ec5a-123">Caso contrário, os objetos na topologia podem não ser desligados corretamente.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-123">Otherwise, objects in the topology might not be shut down correctly.</span></span>

<span data-ttu-id="8ec5a-124">Esse atributo não se aplica quando o aplicativo desliga a sessão de mídia chamando [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="8ec5a-124">This attribute does not apply when the application shuts down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="8ec5a-125">Quando a sessão de mídia é desligada, ela sempre desliga os coletores de mídia e MFTs assíncronas na topologia atual.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-125">When the Media Session shuts down, it always shuts down the media sinks and asynchronous MFTs in the current topology.</span></span>

<span data-ttu-id="8ec5a-126">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ec5a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ec5a-127">Requirements</span></span>



| <span data-ttu-id="8ec5a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ec5a-128">Requirement</span></span> | <span data-ttu-id="8ec5a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8ec5a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec5a-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ec5a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8ec5a-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ec5a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8ec5a-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ec5a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8ec5a-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ec5a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8ec5a-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ec5a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ec5a-135"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec5a-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec5a-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ec5a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec5a-137">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8ec5a-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8ec5a-138">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="8ec5a-138">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="8ec5a-139">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="8ec5a-139">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="8ec5a-140">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8ec5a-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8ec5a-141">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="8ec5a-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8ec5a-142">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="8ec5a-142">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




