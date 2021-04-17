---
description: Especifica quando uma transformação é descarregada.
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: Atributo MF_TOPONODE_DRAIN (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b87d626738b82f4504673392bd0fe159e2722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808318"
---
# <a name="mf_toponode_drain-attribute"></a><span data-ttu-id="79bc5-103">\_Atributo de \_ dreno TOPONODE MF</span><span class="sxs-lookup"><span data-stu-id="79bc5-103">MF\_TOPONODE\_DRAIN attribute</span></span>

<span data-ttu-id="79bc5-104">Especifica quando uma transformação é descarregada.</span><span class="sxs-lookup"><span data-stu-id="79bc5-104">Specifies when a transform is drained.</span></span>

## <a name="data-type"></a><span data-ttu-id="79bc5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="79bc5-105">Data type</span></span>

<span data-ttu-id="79bc5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="79bc5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="79bc5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="79bc5-107">Remarks</span></span>

<span data-ttu-id="79bc5-108">Esse atributo se aplica a nós de transformação (**\_ nó de \_ transformação \_ de topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="79bc5-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="79bc5-109">O valor do atributo é um membro da enumeração do [**\_ modo de \_ descarga \_ TOPONODE MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) .</span><span class="sxs-lookup"><span data-stu-id="79bc5-109">The value of the attribute is a member of the [**MF\_TOPONODE\_DRAIN\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) enumeration.</span></span> <span data-ttu-id="79bc5-110">Se esse atributo não for definido, o valor padrão será **o \_ \_ \_ padrão MF TOPONODE de dreno**.</span><span class="sxs-lookup"><span data-stu-id="79bc5-110">If this attribute is not set, the default value is **MF\_TOPONODE\_DRAIN\_DEFAULT**.</span></span>

<span data-ttu-id="79bc5-111">O descarregamento é executado chamando [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) na transformação com a mensagem [**MFT \_ \_ comando de \_ drenagem**](mft-message-command-drain.md) .</span><span class="sxs-lookup"><span data-stu-id="79bc5-111">Draining is performed by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the transform with the [**MFT\_MESSAGE\_COMMAND\_DRAIN**](mft-message-command-drain.md) message.</span></span> <span data-ttu-id="79bc5-112">Para obter mais informações, consulte Enumeração de [**\_ \_ tipo de mensagem MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .</span><span class="sxs-lookup"><span data-stu-id="79bc5-112">For more information, see [**MFT\_MESSAGE\_TYPE**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) enumeration.</span></span>

<span data-ttu-id="79bc5-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="79bc5-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="79bc5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79bc5-114">Requirements</span></span>



| <span data-ttu-id="79bc5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="79bc5-115">Requirement</span></span> | <span data-ttu-id="79bc5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="79bc5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79bc5-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79bc5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79bc5-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79bc5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="79bc5-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79bc5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="79bc5-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79bc5-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="79bc5-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79bc5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="79bc5-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="79bc5-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79bc5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="79bc5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79bc5-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79bc5-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="79bc5-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="79bc5-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="79bc5-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="79bc5-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="79bc5-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="79bc5-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="79bc5-128">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="79bc5-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




