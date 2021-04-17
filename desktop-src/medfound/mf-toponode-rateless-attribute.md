---
description: Especifica se o coletor de mídia associado a este nó de topologia é sem taxa.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: Atributo MF_TOPONODE_RATELESS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5c5ded4d8d09e8d45f766b03737954329c9202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791587"
---
# <a name="mf_toponode_rateless-attribute"></a><span data-ttu-id="3fc9f-103">\_Atributo MF TOPONODE sem \_ taxa</span><span class="sxs-lookup"><span data-stu-id="3fc9f-103">MF\_TOPONODE\_RATELESS attribute</span></span>

<span data-ttu-id="3fc9f-104">Especifica se o coletor de mídia associado a este nó de topologia é sem taxa.</span><span class="sxs-lookup"><span data-stu-id="3fc9f-104">Specifies whether the media sink associated with this topology node is rateless.</span></span>

## <a name="data-type"></a><span data-ttu-id="3fc9f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3fc9f-105">Data type</span></span>

<span data-ttu-id="3fc9f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3fc9f-106">**UINT32**</span></span>

<span data-ttu-id="3fc9f-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="3fc9f-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fc9f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fc9f-108">Remarks</span></span>

<span data-ttu-id="3fc9f-109">Esse atributo se aplica a nós de saída (**\_ nó de \_ saída \_ da topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="3fc9f-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="3fc9f-110">Se o valor desse atributo for diferente de zero, a sessão de mídia tratará o coletor de mídia como um coletor sem taxas, independentemente de o coletor de mídia retornar a característica sem **\_ taxa de MEDIASINK** .</span><span class="sxs-lookup"><span data-stu-id="3fc9f-110">If the value of this attribute is nonzero, the Media Session treats the media sink as a rateless sink, regardless of whether the media sink returns the **MEDIASINK\_RATELESS** characteristic.</span></span> <span data-ttu-id="3fc9f-111">Se esse atributo não estiver definido, supõe-se que o coletor de mídia não seja sem taxa.</span><span class="sxs-lookup"><span data-stu-id="3fc9f-111">If this attribute is not set, the media sink is assumed not to be rateless.</span></span>

<span data-ttu-id="3fc9f-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3fc9f-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fc9f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fc9f-113">Requirements</span></span>



| <span data-ttu-id="3fc9f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fc9f-114">Requirement</span></span> | <span data-ttu-id="3fc9f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3fc9f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc9f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fc9f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3fc9f-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fc9f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3fc9f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fc9f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3fc9f-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3fc9f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3fc9f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fc9f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fc9f-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fc9f-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fc9f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fc9f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fc9f-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3fc9f-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3fc9f-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3fc9f-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3fc9f-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="3fc9f-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3fc9f-126">**IMFMediaSink:: getcaracterísticas**</span><span class="sxs-lookup"><span data-stu-id="3fc9f-126">**IMFMediaSink::GetCharacteristics**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[<span data-ttu-id="3fc9f-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="3fc9f-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="3fc9f-128">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="3fc9f-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




