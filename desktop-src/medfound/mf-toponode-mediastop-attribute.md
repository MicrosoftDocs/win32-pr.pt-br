---
description: Especifica a hora de parada da apresentação.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: Atributo MF_TOPONODE_MEDIASTOP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5b763d1d5adabc520900dde6839d1599ddcb3d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105761563"
---
# <a name="mf_toponode_mediastop-attribute"></a><span data-ttu-id="1ec9c-103">\_Atributo MF TOPONODE \_ MEDIASTOP</span><span class="sxs-lookup"><span data-stu-id="1ec9c-103">MF\_TOPONODE\_MEDIASTOP attribute</span></span>

<span data-ttu-id="1ec9c-104">Especifica a hora de parada da apresentação.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-104">Specifies the stop time of the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="1ec9c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1ec9c-105">Data type</span></span>

<span data-ttu-id="1ec9c-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1ec9c-106">**UINT64**</span></span>

<span data-ttu-id="1ec9c-107">Tratar como um valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="1ec9c-107">Treat as a **LONGLONG** value.</span></span>

## <a name="getset"></a><span data-ttu-id="1ec9c-108">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="1ec9c-108">Get/set</span></span>

<span data-ttu-id="1ec9c-109">Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="1ec9c-109">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="1ec9c-110">Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="1ec9c-110">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="1ec9c-111">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="1ec9c-111">Applies to</span></span>

[<span data-ttu-id="1ec9c-112">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="1ec9c-112">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a><span data-ttu-id="1ec9c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ec9c-113">Remarks</span></span>

<span data-ttu-id="1ec9c-114">Esse atributo especifica a posição na origem em que a reprodução é interrompida, em unidades de 100 nanossegundos, em relação ao início da origem.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-114">This attribute specifies the position in the source where playback stops, in 100-nanosecond units, relative to the start the source.</span></span> <span data-ttu-id="1ec9c-115">Se o atributo não estiver definido, a reprodução será interrompida no final da origem.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-115">If the attribute is not set, playback stops at the end of the source.</span></span> <span data-ttu-id="1ec9c-116">Por exemplo, para parar a reprodução na marca de 5 segundos, defina esse atributo como 50 milhões.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-116">For example, to stop playback at the 5-second mark, set this attribute to 50000000.</span></span> <span data-ttu-id="1ec9c-117">Defina o atributo nos nós de origem na topologia (nós com tipo igual a **SOURCESTREAM de \_ topologia \_ \_ MF**).</span><span class="sxs-lookup"><span data-stu-id="1ec9c-117">Set the attribute on the source nodes in the topology (nodes with type equal to **MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="1ec9c-118">Defina o atributo antes de chamar [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="1ec9c-118">Set the attribute before calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

> [!Note]  
> <span data-ttu-id="1ec9c-119">Se você inserir manualmente um decodificador na topologia, também deverá definir os atributos de [TOPONODE do MF \_ \_ \_ aqui](mf-toponode-markin-here-attribute.md) e do [MF \_ TOPONODE \_ \_ markout](mf-toponode-markout-here-attribute.md) no nó do decodificador.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-119">If you manually insert a decoder into the topology, you must also set the [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) and [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) attributes on the decoder node.</span></span>

 

<span data-ttu-id="1ec9c-120">Depois que a topologia for definida, a definição desse atributo não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-120">After the topology is set, setting this attribute has no effect.</span></span>

<span data-ttu-id="1ec9c-121">Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-121">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="1ec9c-122">No entanto, os valores negativos não são significativos.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-122">However, negative values are not meaningful.</span></span>

<span data-ttu-id="1ec9c-123">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1ec9c-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec9c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ec9c-124">Requirements</span></span>



| <span data-ttu-id="1ec9c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec9c-125">Requirement</span></span> | <span data-ttu-id="1ec9c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1ec9c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec9c-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ec9c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec9c-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ec9c-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1ec9c-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ec9c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec9c-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1ec9c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1ec9c-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ec9c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ec9c-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec9c-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec9c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ec9c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec9c-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ec9c-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ec9c-135">Tempos de apresentação da sequência</span><span class="sxs-lookup"><span data-stu-id="1ec9c-135">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="1ec9c-136">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="1ec9c-136">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ec9c-137">**\_TOPONODE MF \_ MEDIASTART**</span><span class="sxs-lookup"><span data-stu-id="1ec9c-137">**MF\_TOPONODE\_MEDIASTART**</span></span>](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 




