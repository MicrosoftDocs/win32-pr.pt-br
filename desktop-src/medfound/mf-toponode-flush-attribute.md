---
description: Especifica quando uma transformação é liberada.
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: Atributo MF_TOPONODE_FLUSH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea241227d70d967f6f41ccd994176e9ddbbacbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785251"
---
# <a name="mf_toponode_flush-attribute"></a><span data-ttu-id="c1558-103">\_Atributo de \_ liberação MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="c1558-103">MF\_TOPONODE\_FLUSH attribute</span></span>

<span data-ttu-id="c1558-104">Especifica quando uma transformação é liberada.</span><span class="sxs-lookup"><span data-stu-id="c1558-104">Specifies when a transform is flushed.</span></span>

## <a name="data-type"></a><span data-ttu-id="c1558-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c1558-105">Data type</span></span>

<span data-ttu-id="c1558-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c1558-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c1558-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1558-107">Remarks</span></span>

<span data-ttu-id="c1558-108">Esse atributo se aplica a nós de transformação (**\_ nó de \_ transformação \_ de topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="c1558-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="c1558-109">O valor do atributo é um membro da enumeração do [**\_ modo de \_ liberação \_ MF TOPONODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) .</span><span class="sxs-lookup"><span data-stu-id="c1558-109">The value of the attribute is a member of the [**MF\_TOPONODE\_FLUSH\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) enumeration.</span></span> <span data-ttu-id="c1558-110">Se esse atributo não estiver definido, o valor padrão será **\_ TOPONODE de \_ movimentação \_ de MF sempre**.</span><span class="sxs-lookup"><span data-stu-id="c1558-110">If this attribute is not set, the default value is **MF\_TOPONODE\_FLUSH\_ALWAYS**.</span></span>

<span data-ttu-id="c1558-111">A liberação é executada chamando [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) na transformação com a mensagem de [**\_ liberação de \_ comando \_ da mensagem MFT**](mft-message-command-flush.md) .</span><span class="sxs-lookup"><span data-stu-id="c1558-111">Flushing is performed by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the transform with the [**MFT\_MESSAGE\_COMMAND\_FLUSH**](mft-message-command-flush.md) message.</span></span> <span data-ttu-id="c1558-112">Para obter mais informações, consulte Enumeração de [**\_ \_ tipo de mensagem MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .</span><span class="sxs-lookup"><span data-stu-id="c1558-112">For more information, see [**MFT\_MESSAGE\_TYPE**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) enumeration.</span></span>

<span data-ttu-id="c1558-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c1558-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1558-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1558-114">Requirements</span></span>



| <span data-ttu-id="c1558-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1558-115">Requirement</span></span> | <span data-ttu-id="c1558-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c1558-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1558-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1558-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c1558-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1558-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c1558-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1558-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c1558-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1558-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c1558-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1558-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1558-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1558-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1558-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1558-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1558-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c1558-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1558-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c1558-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c1558-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="c1558-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c1558-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="c1558-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="c1558-128">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="c1558-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




