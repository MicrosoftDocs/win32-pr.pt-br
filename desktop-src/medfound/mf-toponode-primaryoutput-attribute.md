---
description: Indica qual saída é a saída primária em um nó de t.
ms.assetid: f7d98837-75da-48cc-8307-091be2d95392
title: Atributo MF_TOPONODE_PRIMARYOUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4130f1df4789ad910ae013eab43168983b47c316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296482"
---
# <a name="mf_toponode_primaryoutput-attribute"></a><span data-ttu-id="b74c1-103">\_Atributo MF TOPONODE \_ PrimaryOutput porque</span><span class="sxs-lookup"><span data-stu-id="b74c1-103">MF\_TOPONODE\_PRIMARYOUTPUT attribute</span></span>

<span data-ttu-id="b74c1-104">Indica qual saída é a saída primária em um nó de t.</span><span class="sxs-lookup"><span data-stu-id="b74c1-104">Indicates which output is the primary output on a tee node.</span></span>

## <a name="data-type"></a><span data-ttu-id="b74c1-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b74c1-105">Data type</span></span>

<span data-ttu-id="b74c1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b74c1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b74c1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b74c1-107">Remarks</span></span>

<span data-ttu-id="b74c1-108">Esse atributo se aplica a nós de "t" (**\_ nó de \_ t \_ da topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="b74c1-108">This attribute applies to tee nodes (**MF\_TOPOLOGY\_TEE\_NODE**).</span></span>

<span data-ttu-id="b74c1-109">O valor desse atributo é o índice de base zero de uma conexão de saída neste nó de alto-t.</span><span class="sxs-lookup"><span data-stu-id="b74c1-109">The value of this attribute is the zero-based index of an output connection on this tee node.</span></span> <span data-ttu-id="b74c1-110">Esse valor indica qual saída é o fluxo de saída primário.</span><span class="sxs-lookup"><span data-stu-id="b74c1-110">This value indicates which output is the primary output stream.</span></span> <span data-ttu-id="b74c1-111">O pipeline aguarda uma solicitação da saída primária antes de processar solicitações de outras saídas.</span><span class="sxs-lookup"><span data-stu-id="b74c1-111">The pipeline waits for a request from the primary output before processing requests from the other outputs.</span></span>

<span data-ttu-id="b74c1-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b74c1-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b74c1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b74c1-113">Requirements</span></span>



| <span data-ttu-id="b74c1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b74c1-114">Requirement</span></span> | <span data-ttu-id="b74c1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b74c1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b74c1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b74c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b74c1-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b74c1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b74c1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b74c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b74c1-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b74c1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b74c1-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b74c1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b74c1-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b74c1-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b74c1-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b74c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b74c1-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b74c1-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b74c1-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b74c1-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b74c1-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="b74c1-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b74c1-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="b74c1-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b74c1-127">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="b74c1-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




