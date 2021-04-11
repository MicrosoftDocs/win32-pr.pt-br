---
description: Especifica se o carregador de topologia enumera os tipos de mídia fornecidos pela origem da mídia.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: Atributo MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296311"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a><span data-ttu-id="4822d-103">\_Atributo de \_ tipos de origem de enumeração de topologia MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="4822d-103">MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute</span></span>

<span data-ttu-id="4822d-104">Especifica se o carregador de topologia enumera os tipos de mídia fornecidos pela origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="4822d-104">Specifies whether the topology loader enumerates the media types provided by the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="4822d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4822d-105">Data type</span></span>

<span data-ttu-id="4822d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4822d-106">**UINT32**</span></span>

<span data-ttu-id="4822d-107">Use um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4822d-107">Use one of the following values.</span></span>



| <span data-ttu-id="4822d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4822d-108">Value</span></span>                                                                                                                                    | <span data-ttu-id="4822d-109">Significado</span><span class="sxs-lookup"><span data-stu-id="4822d-109">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="4822d-110"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="4822d-110"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="4822d-111">Não enumere os tipos de mídia de origem.</span><span class="sxs-lookup"><span data-stu-id="4822d-111">Do not enumerate the source media types.</span></span><br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="4822d-112"><dt>VERDADEIRO \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="4822d-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="4822d-113">Enumere os tipos de mídia de origem.</span><span class="sxs-lookup"><span data-stu-id="4822d-113">Enumerate the source media types.</span></span><br/>        |



 

## <a name="getset"></a><span data-ttu-id="4822d-114">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="4822d-114">Get/set</span></span>

<span data-ttu-id="4822d-115">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4822d-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4822d-116">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4822d-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4822d-117">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="4822d-117">Applies to</span></span>

[<span data-ttu-id="4822d-118">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="4822d-118">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="4822d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4822d-119">Remarks</span></span>

<span data-ttu-id="4822d-120">Cada fluxo em uma fonte de mídia pode oferecer mais de um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="4822d-120">Each stream on a media source can offer more than one media type.</span></span> <span data-ttu-id="4822d-121">A lista de tipos é enumerada por meio da interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) no descritor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4822d-121">The list of types is enumerated through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream descriptor.</span></span>

<span data-ttu-id="4822d-122">A ordem na qual o carregador de topologia tenta os tipos de mídia de uma fonte de mídia é controlada por dois atributos:</span><span class="sxs-lookup"><span data-stu-id="4822d-122">The order in which the topology loader tries a media source's media types is controlled by two attributes:</span></span>

-   <span data-ttu-id="4822d-123">O \_ atributo da topologia MF \_ enumerar \_ \_ tipos de origem na topologia.</span><span class="sxs-lookup"><span data-stu-id="4822d-123">The MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute on the topology.</span></span>
-   <span data-ttu-id="4822d-124">O atributo do [**\_ \_ \_ método MF TOPONODE Connect**](mf-toponode-connect-method-attribute.md) no nó de origem.</span><span class="sxs-lookup"><span data-stu-id="4822d-124">The [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node.</span></span>

<span data-ttu-id="4822d-125">Se o \_ atributo de \_ tipos de origem enumerar topologia MF \_ \_ for **false** ou não estiver definido, o carregador de topologia usará o tipo de mídia atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="4822d-125">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **FALSE** or not set, the topology loader uses the stream's current media type.</span></span> <span data-ttu-id="4822d-126">Ele não enumera a lista de tipos possíveis.</span><span class="sxs-lookup"><span data-stu-id="4822d-126">It does not enumerate the list of possible types.</span></span> <span data-ttu-id="4822d-127">Se o tipo de mídia atual for incompatível com o nó de topologia downstream e nenhuma combinação de decodificadores/conversores puder ser encontrada, a resolução da topologia falhará.</span><span class="sxs-lookup"><span data-stu-id="4822d-127">If the current media type is incompatible with the downstream topology node, and no combination of decoders/converters can be found, topology resolution fails.</span></span>

<span data-ttu-id="4822d-128">Se o \_ atributo de \_ tipos de origem enumerar topologia MF \_ \_ for **true**, o carregador de topologia enumerará os tipos de mídia da fonte até encontrar um tipo compatível.</span><span class="sxs-lookup"><span data-stu-id="4822d-128">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **TRUE**, the topology loader enumerates the source's media types until it finds a compatible type.</span></span> <span data-ttu-id="4822d-129">Nesse caso, a ordem exata das operações dependerá se o atributo do [**\_ \_ \_ método MF TOPONODE Connect**](mf-toponode-connect-method-attribute.md) no nó de origem inclui o sinalizador **do \_ MF \_ Connect \_ resolver \_ OUTPUTTYPES independente** .</span><span class="sxs-lookup"><span data-stu-id="4822d-129">In that case, the exact order of operations depends on the whether the [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node includes the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span>

<span data-ttu-id="4822d-130">Se \_ a topologia MF \_ enumerar \_ tipos de origem \_ for **true** e o sinalizador **\_ \_ \_ \_ OUTPUTTYPES de resolução independente do MF Connect** for definido, o carregador de topologia esgotará cada tipo de mídia antes de passar para a próxima, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4822d-130">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** and the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set, the topology loader exhausts each media type before moving to the next, as follows:</span></span>

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

<span data-ttu-id="4822d-131">Se \_ a topologia MF \_ enumerar \_ tipos de origem \_ for **true** , mas o **MF \_ Connect \_ resolver \_ \_ OUTPUTTYPES independente** não estiver definido, o carregador de topologia tentará uma conexão direta com cada tipo de mídia e tentará cada tipo de mídia com conversores e, por fim, tentará cada tipo de mídia com decodificadores:</span><span class="sxs-lookup"><span data-stu-id="4822d-131">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** but **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** is not set, the topology loader tries a direct connection with each media type, then tries each media type with converters, and finally tries each media type with decoders:</span></span>

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

<span data-ttu-id="4822d-132">Se \_ a topologia MF \_ enumerar \_ tipos de origem \_ for **false**, o sinalizador **\_ \_ \_ \_ OUTPUTTYPES de resolução de conexão do MF Connect** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="4822d-132">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is ignored.</span></span>

<span data-ttu-id="4822d-133">O valor padrão da \_ topologia MF \_ enumerar \_ tipos de origem \_ é **false**, para compatibilidade com aplicativos existentes.</span><span class="sxs-lookup"><span data-stu-id="4822d-133">The default value of MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, for compatibility with existing applications.</span></span>

<span data-ttu-id="4822d-134">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4822d-134">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="example"></a><span data-ttu-id="4822d-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4822d-135">Example</span></span>

<span data-ttu-id="4822d-136">Aqui está um exemplo que ilustra o **sinalizador \_ \_ \_ \_ OUTPUTTYPES de resolução independente do MF Connect** .</span><span class="sxs-lookup"><span data-stu-id="4822d-136">Here is an example that illustrates the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span> <span data-ttu-id="4822d-137">Suponha que a topologia tenha o \_ \_ atributo de tipos de origem enumerar topologia MF \_ \_ definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="4822d-137">Assume the topology has the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute set to **TRUE**.</span></span>

<span data-ttu-id="4822d-138">A origem de mídia oferece os seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="4822d-138">The media source offers the following types:</span></span>

-   <span data-ttu-id="4822d-139">T1, T2, T3</span><span class="sxs-lookup"><span data-stu-id="4822d-139">T1, T2, T3</span></span>

<span data-ttu-id="4822d-140">O coletor de mídia aceita os seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="4822d-140">The media sink accepts the following types:</span></span>

-   <span data-ttu-id="4822d-141">T3, T4</span><span class="sxs-lookup"><span data-stu-id="4822d-141">T3, T4</span></span>

<span data-ttu-id="4822d-142">Caso 1: o sinalizador de **OUTPUTTYPES do MF \_ Connect de \_ resolução \_ independente \_** está definido.</span><span class="sxs-lookup"><span data-stu-id="4822d-142">Case 1: The **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set.</span></span>

1.  <span data-ttu-id="4822d-143">O carregador de topologia tenta uma conexão direta com T1.</span><span class="sxs-lookup"><span data-stu-id="4822d-143">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="4822d-144">O coletor rejeita T1.</span><span class="sxs-lookup"><span data-stu-id="4822d-144">The sink rejects T1.</span></span>
2.  <span data-ttu-id="4822d-145">O carregador de topologia insere um decodificador que aceita T1 e gera T4.</span><span class="sxs-lookup"><span data-stu-id="4822d-145">The topology loader inserts a decoder that accepts T1 and outputs T4.</span></span> <span data-ttu-id="4822d-146">O coletor aceita T4.</span><span class="sxs-lookup"><span data-stu-id="4822d-146">The sink accepts T4.</span></span>
3.  <span data-ttu-id="4822d-147">A topologia final contém: Media Source → Decoder → Media Sink.</span><span class="sxs-lookup"><span data-stu-id="4822d-147">The final topology contains: media source → decoder → media sink.</span></span>

<span data-ttu-id="4822d-148">Caso 2: o sinalizador não está definido.</span><span class="sxs-lookup"><span data-stu-id="4822d-148">Case 2: The flag is not set.</span></span>

1.  <span data-ttu-id="4822d-149">O carregador de topologia tenta uma conexão direta com T1.</span><span class="sxs-lookup"><span data-stu-id="4822d-149">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="4822d-150">O coletor rejeita T1.</span><span class="sxs-lookup"><span data-stu-id="4822d-150">The sink rejects T1.</span></span>
2.  <span data-ttu-id="4822d-151">O carregador de topologia tenta uma conexão direta com T2.</span><span class="sxs-lookup"><span data-stu-id="4822d-151">The topology loader tries a direct connection with T2.</span></span> <span data-ttu-id="4822d-152">O coletor rejeita T2.</span><span class="sxs-lookup"><span data-stu-id="4822d-152">The sink rejects T2.</span></span>
3.  <span data-ttu-id="4822d-153">O carregador de topologia tenta uma conexão direta com T3.</span><span class="sxs-lookup"><span data-stu-id="4822d-153">The topology loader tries a direct connection with T3.</span></span> <span data-ttu-id="4822d-154">O coletor aceita T3.</span><span class="sxs-lookup"><span data-stu-id="4822d-154">The sink accepts T3.</span></span>
4.  <span data-ttu-id="4822d-155">A topologia final contém: Media Source → Media Sink.</span><span class="sxs-lookup"><span data-stu-id="4822d-155">The final topology contains: media source → media sink.</span></span>

## <a name="requirements"></a><span data-ttu-id="4822d-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4822d-156">Requirements</span></span>



| <span data-ttu-id="4822d-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="4822d-157">Requirement</span></span> | <span data-ttu-id="4822d-158">Valor</span><span class="sxs-lookup"><span data-stu-id="4822d-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4822d-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4822d-159">Minimum supported client</span></span><br/> | <span data-ttu-id="4822d-160">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4822d-160">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4822d-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4822d-161">Minimum supported server</span></span><br/> | <span data-ttu-id="4822d-162">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="4822d-162">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4822d-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4822d-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="4822d-164"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4822d-164"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4822d-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="4822d-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4822d-166">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4822d-166">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4822d-167">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="4822d-167">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




