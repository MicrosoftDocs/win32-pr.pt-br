---
description: Atributos de nó de topologia
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Atributos de nó de topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921350"
---
# <a name="topology-node-attributes"></a><span data-ttu-id="9ad9e-103">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="9ad9e-103">Topology Node Attributes</span></span>

<span data-ttu-id="9ad9e-104">Os atributos a seguir se aplicam a nós de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-104">The following attributes apply to topology nodes.</span></span>

## <a name="general-topology-node-attributes"></a><span data-ttu-id="9ad9e-105">Atributos de nó de topologia geral</span><span class="sxs-lookup"><span data-stu-id="9ad9e-105">General Topology Node Attributes</span></span>



| <span data-ttu-id="9ad9e-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="9ad9e-106">Attribute</span></span>                                                                       | <span data-ttu-id="9ad9e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ad9e-107">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ad9e-108">**\_método de \_ conexão MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-108">**MF\_TOPONODE\_CONNECT\_METHOD**</span></span>](mf-toponode-connect-method-attribute.md)   | <span data-ttu-id="9ad9e-109">Especifica como o carregador de topologia conecta esse nó de topologia e se esse nó é opcional.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-109">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>                                                        |
| [<span data-ttu-id="9ad9e-110">**\_decodificador MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-110">**MF\_TOPONODE\_DECODER**</span></span>](mf-toponode-decoder-attribute.md)                  | <span data-ttu-id="9ad9e-111">Especifica se o objeto de um nó topologia é um decodificador.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-111">Specifies whether a toplogy node's object is a decoder.</span></span>                                                                                                  |
| [<span data-ttu-id="9ad9e-112">**\_descriptografador TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-112">**MF\_TOPONODE\_DECRYPTOR**</span></span>](mf-toponode-decryptor-attribute.md)              | <span data-ttu-id="9ad9e-113">Especifica se um objeto subjacente do nó topologia é um descriptografador.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-113">Specifies whether a toplogy node's underlying object is a decryptor.</span></span>                                                                                     |
| [<span data-ttu-id="9ad9e-114">**\_TOPONODE MF \_ Descartado**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-114">**MF\_TOPONODE\_DISCARDABLE**</span></span>](mf-toponode-discardable-attribute.md)          | <span data-ttu-id="9ad9e-115">Especifica se o pipeline pode descartar amostras de um nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-115">Specifies whether the pipeline can drop samples from a topology node.</span></span>                                                                                    |
| [<span data-ttu-id="9ad9e-116">**\_TOPONODE de \_ erro \_ MF**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-116">**MF\_TOPONODE\_ERROR\_MAJORTYPE**</span></span>](mf-toponode-error-majortype-attribute.md) | <span data-ttu-id="9ad9e-117">Contém o tipo de mídia principal para um nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-117">Contains the major media type for a topology node.</span></span> <span data-ttu-id="9ad9e-118">Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-118">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span> |
| [<span data-ttu-id="9ad9e-119">**subtipo de \_ erro MF TOPONODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-119">**MF\_TOPONODE\_ERROR\_SUBTYPE**</span></span>](mf-toponode-error-subtype-attribute.md)     | <span data-ttu-id="9ad9e-120">Contém o subtipo de mídia para um nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-120">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="9ad9e-121">Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-121">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>    |
| [<span data-ttu-id="9ad9e-122">**\_código de TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-122">**MF\_TOPONODE\_ERRORCODE**</span></span>](mf-toponode-errorcode-attribute.md)              | <span data-ttu-id="9ad9e-123">Contém o código de erro da falha de conexão mais recente para esse nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-123">Contains the error code from the most recent connection failure for this topology node.</span></span>                                                                  |
| [<span data-ttu-id="9ad9e-124">**\_TOPONODE MF \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-124">**MF\_TOPONODE\_LOCKED**</span></span>](mf-toponode-locked-attribute.md)                    | <span data-ttu-id="9ad9e-125">Especifica se os tipos de mídia podem ser alterados neste nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-125">Specifies whether the media types can be changed on this topology node.</span></span>                                                                                  |
| [<span data-ttu-id="9ad9e-126">**\_Mark TOPONODE do MF \_ \_ aqui**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-126">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)         | <span data-ttu-id="9ad9e-127">Especifica se o pipeline aplica o marca-in neste nó.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-127">Specifies whether the pipeline applies mark-in at this node.</span></span>                                                                                             |
| [<span data-ttu-id="9ad9e-128">**\_marcação de TOPONODE MF \_ \_ aqui**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-128">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)       | <span data-ttu-id="9ad9e-129">Especifica se o pipeline aplica a marcação neste nó.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-129">Specifies whether the pipeline applies mark-out at this node.</span></span>                                                                                            |



 

## <a name="source-node-attributes"></a><span data-ttu-id="9ad9e-130">Atributos do nó de origem</span><span class="sxs-lookup"><span data-stu-id="9ad9e-130">Source Node Attributes</span></span>



| <span data-ttu-id="9ad9e-131">Atributo</span><span class="sxs-lookup"><span data-stu-id="9ad9e-131">Attribute</span></span>                                                                                       | <span data-ttu-id="9ad9e-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ad9e-132">Description</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ad9e-133">**\_TOPONODE MF \_ MEDIASTART**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-133">**MF\_TOPONODE\_MEDIASTART**</span></span>](mf-toponode-mediastart-attribute.md)                            | <span data-ttu-id="9ad9e-134">Especifica a hora de início de uma apresentação, em relação ao início do arquivo de origem de mídia, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-134">Specifies the start time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="9ad9e-135">**\_TOPONODE MF \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-135">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)                              | <span data-ttu-id="9ad9e-136">Especifica a hora de parada de uma apresentação, em relação ao início do arquivo de origem de mídia, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-136">Specifies the stop time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span>  |
| [<span data-ttu-id="9ad9e-137">**\_ \_ descritor de apresentação do MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-137">**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**</span></span>](mf-toponode-presentation-descriptor-attribute.md) | <span data-ttu-id="9ad9e-138">Contém um ponteiro para o descritor de apresentação para a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-138">Contains a pointer to the presentation descriptor for the media source.</span></span>                                           |
| [<span data-ttu-id="9ad9e-139">**\_elemento de \_ sequência \_ TOPONODE MF**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-139">**MF\_TOPONODE\_SEQUENCE\_ELEMENTID**</span></span>](mf-toponode-sequence-elementid-attribute.md)           | <span data-ttu-id="9ad9e-140">Especifica o elemento que contém um nó de origem.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-140">Specifies the element that contains a source node.</span></span>                                                                |
| [<span data-ttu-id="9ad9e-141">**\_origem MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-141">**MF\_TOPONODE\_SOURCE**</span></span>](mf-toponode-source-attribute.md)                                    | <span data-ttu-id="9ad9e-142">Contém um ponteiro para a fonte de mídia associada a um nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-142">Contains a pointer to the media source associated with a topology node.</span></span>                                           |
| [<span data-ttu-id="9ad9e-143">**\_ \_ descritor de fluxo de TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-143">**MF\_TOPONODE\_STREAM\_DESCRIPTOR**</span></span>](mf-toponode-stream-descriptor-attribute.md)             | <span data-ttu-id="9ad9e-144">Contém um ponteiro para o descritor de fluxo para a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-144">Contains a pointer to the stream descriptor for the media source.</span></span>                                                 |
| [<span data-ttu-id="9ad9e-145">**\_ID da \_ fila de TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-145">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)                       | <span data-ttu-id="9ad9e-146">Especifica uma fila de trabalho para um nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-146">Specifies a work queue for a topology node.</span></span>                                                                       |
| [<span data-ttu-id="9ad9e-147">**\_classe TOPONODE do MF \_ fila do \_ MMCSS \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-147">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)    | <span data-ttu-id="9ad9e-148">Especifica uma tarefa do serviço de Agendador de classes de multimídia (MMCSS) para um nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-148">Specifies a Multimedia Class Scheduler Service (MMCSS) task for a topology node.</span></span>                                  |
| [<span data-ttu-id="9ad9e-149">**\_TaskId TOPONODE \_ fila \_ de \_ tarefas do MMCSS**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-149">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | <span data-ttu-id="9ad9e-150">Especifica um identificador de tarefa do MMCSS para um nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-150">Specifies a MMCSS task identifier for a topology node.</span></span>                                                            |



 

## <a name="transform-node-attributes"></a><span data-ttu-id="9ad9e-151">Atributos de nó de transformação</span><span class="sxs-lookup"><span data-stu-id="9ad9e-151">Transform Node Attributes</span></span>



| <span data-ttu-id="9ad9e-152">Atributo</span><span class="sxs-lookup"><span data-stu-id="9ad9e-152">Attribute</span></span>                                                                             | <span data-ttu-id="9ad9e-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ad9e-153">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ad9e-154">**\_TOPONODE MF \_ D3DAWARE**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-154">**MF\_TOPONODE\_D3DAWARE**</span></span>](mf-toponode-d3daware-attribute.md)                      | <span data-ttu-id="9ad9e-155">Especifica se a transformação associada a um nó de topologia dá suporte a DXVA (aceleração de vídeo do DirectX)</span><span class="sxs-lookup"><span data-stu-id="9ad9e-155">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA)</span></span> |
| [<span data-ttu-id="9ad9e-156">**\_dreno TOPONODE de MF \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-156">**MF\_TOPONODE\_DRAIN**</span></span>](mf-toponode-drain-attribute.md)                            | <span data-ttu-id="9ad9e-157">Especifica quando uma transformação é descarregada.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-157">Specifies when a transform is drained.</span></span>                                                                     |
| [<span data-ttu-id="9ad9e-158">**\_liberação de TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-158">**MF\_TOPONODE\_FLUSH**</span></span>](mf-toponode-flush-attribute.md)                            | <span data-ttu-id="9ad9e-159">Especifica quando uma transformação é liberada.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-159">Specifies when a transform is flushed.</span></span>                                                                     |
| [<span data-ttu-id="9ad9e-160">**\_OBJECTID de \_ transformação \_ TOPONODE MF**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-160">**MF\_TOPONODE\_TRANSFORM\_OBJECTID**</span></span>](mf-toponode-transform-objectid-attribute.md) | <span data-ttu-id="9ad9e-161">O identificador de classe (CLSID) da transformação associada a este nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-161">The class identifier (CLSID) of the transform associated with this topology node.</span></span>                          |



 

## <a name="output-node-attributes"></a><span data-ttu-id="9ad9e-162">Atributos do nó de saída</span><span class="sxs-lookup"><span data-stu-id="9ad9e-162">Output Node Attributes</span></span>



| <span data-ttu-id="9ad9e-163">Atributo</span><span class="sxs-lookup"><span data-stu-id="9ad9e-163">Attribute</span></span>                                                                                  | <span data-ttu-id="9ad9e-164">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ad9e-164">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ad9e-165">**TOPONODE do MF \_ \_ desabilitar o \_ prelance**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-165">**MF\_TOPONODE\_DISABLE\_PREROLL**</span></span>](mf-toponode-disable-preroll-attribute.md)            | <span data-ttu-id="9ad9e-166">Especifica se a sessão de mídia usa a preversão no coletor de mídia representado por esse nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-166">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>            |
| [<span data-ttu-id="9ad9e-167">**MF \_ TOPONODE \_ parashutdown \_ on \_ Remove**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-167">**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**</span></span>](mf-toponode-noshutdown-on-remove-attribute.md) | <span data-ttu-id="9ad9e-168">Especifica se a sessão de mídia desliga o coletor de mídia quando o nó de saída é removido da topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-168">Specifies whether the Media Session shuts down the media sink when the output node is removed from the topology.</span></span> |
| [<span data-ttu-id="9ad9e-169">**MF \_ TOPONODE sem \_ taxa**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-169">**MF\_TOPONODE\_RATELESS**</span></span>](mf-toponode-rateless-attribute.md)                           | <span data-ttu-id="9ad9e-170">Especifica se o coletor de mídia associado a este nó de topologia é sem taxa.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-170">Specifies whether the media sink associated with this topology node is rateless.</span></span>                                 |
| [<span data-ttu-id="9ad9e-171">**\_ \_ streamid TOPONODE MF**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-171">**MF\_TOPONODE\_STREAMID**</span></span>](mf-toponode-streamid-attribute.md)                           | <span data-ttu-id="9ad9e-172">O identificador de fluxo do coletor de fluxo associado a este nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-172">The stream identifier of the stream sink associated with this topology node.</span></span>                                     |



 

## <a name="tee-node-attributes"></a><span data-ttu-id="9ad9e-173">Atributos de nó de t</span><span class="sxs-lookup"><span data-stu-id="9ad9e-173">Tee Node Attributes</span></span>



| <span data-ttu-id="9ad9e-174">Atributo</span><span class="sxs-lookup"><span data-stu-id="9ad9e-174">Attribute</span></span>                                                                  | <span data-ttu-id="9ad9e-175">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ad9e-175">Description</span></span>                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="9ad9e-176">**\_TOPONODE MF \_ PrimaryOutput porque**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-176">**MF\_TOPONODE\_PRIMARYOUTPUT**</span></span>](mf-toponode-primaryoutput-attribute.md) | <span data-ttu-id="9ad9e-177">Indica qual saída é a saída primária em um nó de t.</span><span class="sxs-lookup"><span data-stu-id="9ad9e-177">Indicates which output is the primary output on a tee node.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9ad9e-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ad9e-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ad9e-179">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="9ad9e-179">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="9ad9e-180">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9ad9e-180">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9ad9e-181">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="9ad9e-181">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 



