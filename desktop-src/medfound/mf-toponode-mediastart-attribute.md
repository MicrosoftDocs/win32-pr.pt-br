---
description: Especifica a hora de início da apresentação.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: Atributo MF_TOPONODE_MEDIASTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab00727cc328bfd6ba780050160fb21eecbb96f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105815412"
---
# <a name="mf_toponode_mediastart-attribute"></a><span data-ttu-id="28ea5-103">\_Atributo MF TOPONODE \_ MEDIASTART</span><span class="sxs-lookup"><span data-stu-id="28ea5-103">MF\_TOPONODE\_MEDIASTART attribute</span></span>

<span data-ttu-id="28ea5-104">Especifica a hora de início da apresentação.</span><span class="sxs-lookup"><span data-stu-id="28ea5-104">Specifies the start time of the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="28ea5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="28ea5-105">Data type</span></span>

<span data-ttu-id="28ea5-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="28ea5-106">**UINT64**</span></span>

<span data-ttu-id="28ea5-107">Tratar como um valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="28ea5-107">Treat as a **LONGLONG** value.</span></span>

## <a name="getset"></a><span data-ttu-id="28ea5-108">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="28ea5-108">Get/set</span></span>

<span data-ttu-id="28ea5-109">Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="28ea5-109">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="28ea5-110">Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="28ea5-110">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="28ea5-111">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="28ea5-111">Applies to</span></span>

[<span data-ttu-id="28ea5-112">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="28ea5-112">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a><span data-ttu-id="28ea5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="28ea5-113">Remarks</span></span>

<span data-ttu-id="28ea5-114">Esse atributo especifica a posição na origem em que a reprodução é iniciada, em unidades de 100 nanossegundos, em relação ao início da origem.</span><span class="sxs-lookup"><span data-stu-id="28ea5-114">This attribute specifies the position in the source where playback starts, in 100-nanosecond units, relative to the start the source.</span></span> <span data-ttu-id="28ea5-115">Se o atributo não estiver definido, a reprodução começará em zero (o início do arquivo).</span><span class="sxs-lookup"><span data-stu-id="28ea5-115">If the attribute is not set, playback starts at zero (the start of the file).</span></span> <span data-ttu-id="28ea5-116">Por exemplo, para iniciar a reprodução na marca de 5 segundos, defina esse atributo como 50 milhões.</span><span class="sxs-lookup"><span data-stu-id="28ea5-116">For example, to start playback at the 5-second mark, set this attribute to 50000000.</span></span> <span data-ttu-id="28ea5-117">Defina o atributo nos nós de origem na topologia (nós com tipo igual a **SOURCESTREAM de \_ topologia \_ \_ MF**).</span><span class="sxs-lookup"><span data-stu-id="28ea5-117">Set the attribute on the source nodes in the topology (nodes with type equal to **MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="28ea5-118">Defina o atributo antes de chamar [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="28ea5-118">Set the attribute before calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

> [!Note]  
> <span data-ttu-id="28ea5-119">Se você inserir manualmente um decodificador na topologia, também deverá definir os atributos de [TOPONODE do MF \_ \_ \_ aqui](mf-toponode-markin-here-attribute.md) e do [MF \_ TOPONODE \_ \_ markout](mf-toponode-markout-here-attribute.md) no nó do decodificador.</span><span class="sxs-lookup"><span data-stu-id="28ea5-119">If you manually insert a decoder into the topology, you must also set the [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) and [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) attributes on the decoder node.</span></span>

 

<span data-ttu-id="28ea5-120">Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="28ea5-120">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="28ea5-121">No entanto, os valores negativos não são significativos.</span><span class="sxs-lookup"><span data-stu-id="28ea5-121">However, negative values are not meaningful.</span></span>

<span data-ttu-id="28ea5-122">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="28ea5-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="28ea5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28ea5-123">Requirements</span></span>



| <span data-ttu-id="28ea5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="28ea5-124">Requirement</span></span> | <span data-ttu-id="28ea5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="28ea5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28ea5-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28ea5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="28ea5-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28ea5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="28ea5-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28ea5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="28ea5-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28ea5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="28ea5-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28ea5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="28ea5-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28ea5-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28ea5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="28ea5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ea5-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="28ea5-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="28ea5-134">Tempos de apresentação da sequência</span><span class="sxs-lookup"><span data-stu-id="28ea5-134">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="28ea5-135">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="28ea5-135">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="28ea5-136">**\_TOPONODE MF \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="28ea5-136">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




