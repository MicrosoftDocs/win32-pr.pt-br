---
description: Especifica se um objeto subjacente de nós topologia é um Decrypter.
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: Atributo MF_TOPONODE_DECRYPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a8129e82fc2ebc01ee8cf21aabda77dc26970e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765291"
---
# <a name="mf_toponode_decryptor-attribute"></a><span data-ttu-id="0f3a4-103">\_Atributo de \_ descriptografia TOPONODE MF</span><span class="sxs-lookup"><span data-stu-id="0f3a4-103">MF\_TOPONODE\_DECRYPTOR attribute</span></span>

<span data-ttu-id="0f3a4-104">Especifica se o objeto subjacente de um nó topologia é um Decrypter.</span><span class="sxs-lookup"><span data-stu-id="0f3a4-104">Specifies whether a toplogy node's underlying object is a decrypter.</span></span>

## <a name="data-type"></a><span data-ttu-id="0f3a4-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0f3a4-105">Data type</span></span>

<span data-ttu-id="0f3a4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0f3a4-106">**UINT32**</span></span>

<span data-ttu-id="0f3a4-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="0f3a4-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f3a4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f3a4-108">Remarks</span></span>

<span data-ttu-id="0f3a4-109">Esse atributo se aplica a todos os tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="0f3a4-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="0f3a4-110">Se o valor desse atributo for diferente de zero, o objeto subjacente do nó será um Decrypter.</span><span class="sxs-lookup"><span data-stu-id="0f3a4-110">If the value of this attribute is nonzero, the node's underlying object is a decrypter.</span></span>

<span data-ttu-id="0f3a4-111">Normalmente, os aplicativos não usam esse atributo diretamente.</span><span class="sxs-lookup"><span data-stu-id="0f3a4-111">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="0f3a4-112">A sessão de mídia define esse atributo quando ele cria um nó para um Decrypter, obtido do método [**IMFInputTrustAuthority:: Getdescriptografar**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) .</span><span class="sxs-lookup"><span data-stu-id="0f3a4-112">The Media Session sets this attribute when it creates a node for a decrypter, obtained from the [**IMFInputTrustAuthority::GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) method.</span></span>

<span data-ttu-id="0f3a4-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0f3a4-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3a4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f3a4-114">Requirements</span></span>



| <span data-ttu-id="0f3a4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f3a4-115">Requirement</span></span> | <span data-ttu-id="0f3a4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0f3a4-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3a4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f3a4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3a4-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f3a4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0f3a4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f3a4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3a4-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0f3a4-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0f3a4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f3a4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f3a4-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f3a4-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f3a4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f3a4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3a4-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f3a4-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0f3a4-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0f3a4-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0f3a4-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="0f3a4-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0f3a4-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="0f3a4-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="0f3a4-128">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="0f3a4-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




