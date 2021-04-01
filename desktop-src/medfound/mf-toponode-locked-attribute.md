---
description: Especifica se os tipos de mídia podem ser alterados neste nó de topologia.
ms.assetid: 8805ed63-1408-40bc-bb82-f3c51576dfa4
title: Atributo MF_TOPONODE_LOCKED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70776b1a5ba9c5c35cd2a2d97618de4b3a65abb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647566"
---
# <a name="mf_toponode_locked-attribute"></a><span data-ttu-id="a6050-103">\_Atributo TOPONODE MF \_ bloqueado</span><span class="sxs-lookup"><span data-stu-id="a6050-103">MF\_TOPONODE\_LOCKED attribute</span></span>

<span data-ttu-id="a6050-104">Especifica se os tipos de mídia podem ser alterados neste nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="a6050-104">Specifies whether the media types can be changed on this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="a6050-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a6050-105">Data type</span></span>

<span data-ttu-id="a6050-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a6050-106">**UINT32**</span></span>

<span data-ttu-id="a6050-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="a6050-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6050-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6050-108">Remarks</span></span>

<span data-ttu-id="a6050-109">Esse atributo se aplica a todos os tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="a6050-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="a6050-110">Se o valor desse atributo for diferente de zero, o carregador de topologia não alterará os tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="a6050-110">If value of this attribute is nonzero, the topology loader will not change the media types.</span></span> <span data-ttu-id="a6050-111">Esse atributo é definido como **true** quando o nó está em uso.</span><span class="sxs-lookup"><span data-stu-id="a6050-111">This attribute is set to **TRUE** when the node is in use.</span></span>

<span data-ttu-id="a6050-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a6050-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6050-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6050-113">Requirements</span></span>



| <span data-ttu-id="a6050-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6050-114">Requirement</span></span> | <span data-ttu-id="a6050-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a6050-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6050-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6050-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a6050-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6050-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a6050-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6050-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a6050-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6050-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a6050-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6050-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6050-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6050-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6050-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6050-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6050-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6050-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a6050-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a6050-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a6050-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="a6050-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a6050-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="a6050-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="a6050-127">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="a6050-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




