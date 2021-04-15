---
description: O identificador de classe (CLSID) da Media Foundation transformação (MFT) associada a esse nó de topologia.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: Atributo MF_TOPONODE_TRANSFORM_OBJECTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502111"
---
# <a name="mf_toponode_transform_objectid-attribute"></a><span data-ttu-id="0e42d-103">\_Atributo de \_ OBJECTID de transformação MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="0e42d-103">MF\_TOPONODE\_TRANSFORM\_OBJECTID attribute</span></span>

<span data-ttu-id="0e42d-104">O identificador de classe (CLSID) da Media Foundation transformação (MFT) associada a esse nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="0e42d-104">The class identifier (CLSID) of the Media Foundation transform (MFT) associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="0e42d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0e42d-105">Data type</span></span>

<span data-ttu-id="0e42d-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="0e42d-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="0e42d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e42d-107">Remarks</span></span>

<span data-ttu-id="0e42d-108">Esse atributo se aplica a nós de transformação (**\_ nó de \_ transformação \_ de topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="0e42d-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="0e42d-109">Os aplicativos podem usar esse atributo para inicializar um nó de Transbase.</span><span class="sxs-lookup"><span data-stu-id="0e42d-109">Applications can use this attribute to initialize a transfrom node.</span></span> <span data-ttu-id="0e42d-110">Se você definir esse atributo, não precisará chamar [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) com um ponteiro para um objeto de ativação ou MFT.</span><span class="sxs-lookup"><span data-stu-id="0e42d-110">If you set this attribute, you do not have to call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) with a pointer to an MFT or activation object.</span></span> <span data-ttu-id="0e42d-111">Por outro lado, se você chamar **setObject**, não precisará definir esse atributo.</span><span class="sxs-lookup"><span data-stu-id="0e42d-111">Conversely, if you call **SetObject**, you do not need to set this attribute.</span></span> <span data-ttu-id="0e42d-112">Para obter mais informações, consulte [criando topologias](creating-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="0e42d-112">For more information, see [Creating Topologies](creating-topologies.md).</span></span>

<span data-ttu-id="0e42d-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0e42d-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e42d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e42d-114">Requirements</span></span>



| <span data-ttu-id="0e42d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e42d-115">Requirement</span></span> | <span data-ttu-id="0e42d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0e42d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e42d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e42d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0e42d-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e42d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0e42d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e42d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0e42d-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e42d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0e42d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e42d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e42d-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e42d-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e42d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e42d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e42d-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e42d-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0e42d-125">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="0e42d-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="0e42d-126">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="0e42d-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="0e42d-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="0e42d-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="0e42d-128">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e42d-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0e42d-129">Criando topologias</span><span class="sxs-lookup"><span data-stu-id="0e42d-129">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="0e42d-130">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="0e42d-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




