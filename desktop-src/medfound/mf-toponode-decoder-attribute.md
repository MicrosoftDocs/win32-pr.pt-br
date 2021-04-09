---
description: Especifica se um objeto subjacente de nós de topologia é um decodificador.
ms.assetid: b6d576dc-b12f-49bf-b938-db2c629df400
title: Atributo MF_TOPONODE_DECODER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab16d14a91608fb6b21c901e3fb055ce5e4dfbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171603"
---
# <a name="mf_toponode_decoder-attribute"></a><span data-ttu-id="4ab23-103">\_Atributo de \_ decodificador MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="4ab23-103">MF\_TOPONODE\_DECODER attribute</span></span>

<span data-ttu-id="4ab23-104">Especifica se um objeto subjacente do nó de topologia é um decodificador.</span><span class="sxs-lookup"><span data-stu-id="4ab23-104">Specifies whether a topology node's underlying object is a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="4ab23-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4ab23-105">Data type</span></span>

<span data-ttu-id="4ab23-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4ab23-106">**UINT32**</span></span>

<span data-ttu-id="4ab23-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="4ab23-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ab23-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ab23-108">Remarks</span></span>

<span data-ttu-id="4ab23-109">Esse atributo se aplica a todos os tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="4ab23-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="4ab23-110">Se o valor desse atributo for diferente de zero, o objeto subjacente do nó será um decodificador.</span><span class="sxs-lookup"><span data-stu-id="4ab23-110">If the value of this attribute is nonzero, the node's underlying object is a decoder.</span></span>

<span data-ttu-id="4ab23-111">O carregador de topologia define esse atributo quando ele cria um nó de decodificador.</span><span class="sxs-lookup"><span data-stu-id="4ab23-111">The topology loader sets this attribute when it creates a decoder node.</span></span> <span data-ttu-id="4ab23-112">Um aplicativo deve definir esse atributo se o aplicativo adicionar manualmente um decodificador à topologia.</span><span class="sxs-lookup"><span data-stu-id="4ab23-112">An application should set this attribute if the application manually adds a decoder to the topology.</span></span>

<span data-ttu-id="4ab23-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4ab23-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ab23-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ab23-114">Requirements</span></span>



| <span data-ttu-id="4ab23-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ab23-115">Requirement</span></span> | <span data-ttu-id="4ab23-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4ab23-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab23-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ab23-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4ab23-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ab23-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4ab23-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ab23-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4ab23-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ab23-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4ab23-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ab23-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ab23-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ab23-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ab23-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ab23-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ab23-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ab23-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ab23-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4ab23-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4ab23-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="4ab23-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4ab23-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="4ab23-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="4ab23-128">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="4ab23-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




