---
description: Especifica como o carregador de topologia conecta esse nó de topologia e se esse nó é opcional.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: Atributo MF_TOPONODE_CONNECT_METHOD (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171331"
---
# <a name="mf_toponode_connect_method-attribute"></a><span data-ttu-id="c97fb-103">\_Atributo do método MF TOPONODE \_ Connect \_</span><span class="sxs-lookup"><span data-stu-id="c97fb-103">MF\_TOPONODE\_CONNECT\_METHOD attribute</span></span>

<span data-ttu-id="c97fb-104">Especifica como o carregador de topologia conecta esse nó de topologia e se esse nó é opcional.</span><span class="sxs-lookup"><span data-stu-id="c97fb-104">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>

## <a name="data-type"></a><span data-ttu-id="c97fb-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c97fb-105">Data type</span></span>

<span data-ttu-id="c97fb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c97fb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c97fb-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c97fb-107">Remarks</span></span>

<span data-ttu-id="c97fb-108">Esse atributo se aplica a todos os tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="c97fb-108">This attribute applies to all node types.</span></span>

<span data-ttu-id="c97fb-109">O valor do atributo é um bit a bit **ou** dos sinalizadores da enumeração do [**\_ \_ método de conexão MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) .</span><span class="sxs-lookup"><span data-stu-id="c97fb-109">The attribute value is a bitwise **OR** of flags from the [**MF\_CONNECT\_METHOD**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) enumeration.</span></span> <span data-ttu-id="c97fb-110">Se esse atributo não for definido, o valor padrão será **MF \_ Connect \_ permitir \_ decodificador**.</span><span class="sxs-lookup"><span data-stu-id="c97fb-110">If this attribute is not set, the default value is **MF\_CONNECT\_ALLOW\_DECODER**.</span></span>

<span data-ttu-id="c97fb-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c97fb-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c97fb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c97fb-112">Requirements</span></span>



| <span data-ttu-id="c97fb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c97fb-113">Requirement</span></span> | <span data-ttu-id="c97fb-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c97fb-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c97fb-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c97fb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c97fb-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c97fb-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c97fb-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c97fb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c97fb-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c97fb-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c97fb-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c97fb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c97fb-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c97fb-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c97fb-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c97fb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97fb-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c97fb-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c97fb-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c97fb-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c97fb-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="c97fb-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c97fb-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="c97fb-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="c97fb-126">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="c97fb-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




