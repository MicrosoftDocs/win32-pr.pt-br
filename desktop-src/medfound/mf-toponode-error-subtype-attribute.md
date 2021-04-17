---
description: Contém o subtipo de mídia para um nó de topologia. Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: Atributo MF_TOPONODE_ERROR_SUBTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1233fb62c271a6f4fd84ec8b2c0b34aa6c49b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798203"
---
# <a name="mf_toponode_error_subtype-attribute"></a><span data-ttu-id="2ddc0-104">\_Atributo de \_ subtipo de erro MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="2ddc0-104">MF\_TOPONODE\_ERROR\_SUBTYPE attribute</span></span>

<span data-ttu-id="2ddc0-105">Contém o subtipo de mídia para um nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="2ddc0-105">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="2ddc0-106">Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto.</span><span class="sxs-lookup"><span data-stu-id="2ddc0-106">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>

## <a name="data-type"></a><span data-ttu-id="2ddc0-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2ddc0-107">Data type</span></span>

<span data-ttu-id="2ddc0-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="2ddc0-108">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="2ddc0-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ddc0-109">Remarks</span></span>

<span data-ttu-id="2ddc0-110">Esse atributo se aplica a todos os tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="2ddc0-110">This attribute applies to all node types.</span></span>

<span data-ttu-id="2ddc0-111">O carregador de topologia pode definir o atributo.</span><span class="sxs-lookup"><span data-stu-id="2ddc0-111">The topology loader might set the attribute.</span></span> <span data-ttu-id="2ddc0-112">Normalmente, os aplicativos lêem esse atributo, mas não os definem.</span><span class="sxs-lookup"><span data-stu-id="2ddc0-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="2ddc0-113">Para obter uma lista de valores possíveis, consulte [GUIDs de tipo de mídia](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="2ddc0-113">For a list of possible values, see [Media Type GUIDs](media-type-guids.md).</span></span>

<span data-ttu-id="2ddc0-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2ddc0-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ddc0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ddc0-115">Requirements</span></span>



| <span data-ttu-id="2ddc0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ddc0-116">Requirement</span></span> | <span data-ttu-id="2ddc0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2ddc0-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddc0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ddc0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2ddc0-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ddc0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2ddc0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ddc0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2ddc0-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2ddc0-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2ddc0-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ddc0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ddc0-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ddc0-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ddc0-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ddc0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ddc0-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2ddc0-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2ddc0-126">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="2ddc0-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="2ddc0-127">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="2ddc0-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="2ddc0-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="2ddc0-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="2ddc0-129">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="2ddc0-129">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




