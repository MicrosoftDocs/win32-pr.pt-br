---
description: Especifica se o pipeline pode descartar amostras de um nó de topologia.
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: Atributo MF_TOPONODE_DISCARDABLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765170"
---
# <a name="mf_toponode_discardable-attribute"></a><span data-ttu-id="fb56a-103">\_Atributo de TOPONODE MF \_</span><span class="sxs-lookup"><span data-stu-id="fb56a-103">MF\_TOPONODE\_DISCARDABLE attribute</span></span>

<span data-ttu-id="fb56a-104">Especifica se o pipeline pode descartar amostras de um nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="fb56a-104">Specifies whether the pipeline can drop samples from a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="fb56a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fb56a-105">Data type</span></span>

<span data-ttu-id="fb56a-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="fb56a-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="fb56a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb56a-107">Remarks</span></span>

<span data-ttu-id="fb56a-108">Esse atributo se aplica a todos os tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="fb56a-108">This attribute applies to all node types.</span></span> <span data-ttu-id="fb56a-109">Normalmente, você definiria esse atributo em nós de baixo e para indicar que as saídas secundárias não são essenciais.</span><span class="sxs-lookup"><span data-stu-id="fb56a-109">Typically you would set this attribute on tee nodes, to indicate that the secondary outputs are not essential.</span></span>

<span data-ttu-id="fb56a-110">O valor do atributo é uma matriz de índices para fluxos de saída no nó.</span><span class="sxs-lookup"><span data-stu-id="fb56a-110">The value of the attribute is an array of indexes to output streams on the node.</span></span>

<span data-ttu-id="fb56a-111">Se esse atributo for definido, o pipeline poderá descartar amostras dos fluxos de saída especificados, se o fluxo estiver atrasado.</span><span class="sxs-lookup"><span data-stu-id="fb56a-111">If this attribute is set, the pipeline might drop samples from the specified output streams, if the stream is falling behind.</span></span>

<span data-ttu-id="fb56a-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="fb56a-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb56a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb56a-113">Requirements</span></span>



| <span data-ttu-id="fb56a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb56a-114">Requirement</span></span> | <span data-ttu-id="fb56a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fb56a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb56a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb56a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fb56a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb56a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fb56a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb56a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fb56a-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb56a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fb56a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb56a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb56a-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb56a-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb56a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb56a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb56a-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb56a-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fb56a-124">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="fb56a-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="fb56a-125">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="fb56a-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="fb56a-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="fb56a-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="fb56a-127">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="fb56a-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




