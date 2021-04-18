---
description: Identifica o nó de topologia para um coletor de fluxo.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: Atributo MF_EVENT_OUTPUT_NODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c484ea55841f4057bf0855dd51b90db951acb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754897"
---
# <a name="mf_event_output_node-attribute"></a><span data-ttu-id="9797d-103">\_Atributo de \_ nó de saída de evento MF \_</span><span class="sxs-lookup"><span data-stu-id="9797d-103">MF\_EVENT\_OUTPUT\_NODE attribute</span></span>

<span data-ttu-id="9797d-104">Identifica o nó de topologia para um coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="9797d-104">Identifies the topology node for a stream sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="9797d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9797d-105">Data type</span></span>

<span data-ttu-id="9797d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="9797d-106">**UINT64**</span></span>

<span data-ttu-id="9797d-107">Tratar como [**TOPOID**](topoid.md).</span><span class="sxs-lookup"><span data-stu-id="9797d-107">Treat as [**TOPOID**](topoid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9797d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="9797d-108">Remarks</span></span>

<span data-ttu-id="9797d-109">O valor desse atributo é um identificador de nó para um nó de saída na topologia atual.</span><span class="sxs-lookup"><span data-stu-id="9797d-109">The value of this attribute is a node identifier for an output node on the current topology.</span></span> <span data-ttu-id="9797d-110">Para obter um ponteiro para o nó associado, chame [**IMFTopology:: GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) na topologia.</span><span class="sxs-lookup"><span data-stu-id="9797d-110">To get a pointer to the associated node, call [**IMFTopology::GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) on the topology.</span></span>

<span data-ttu-id="9797d-111">Esse atributo é usado com os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="9797d-111">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="9797d-112">MESessionStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="9797d-112">MESessionStreamSinkFormatChanged</span></span>](mesessionstreamsinkformatchanged.md)
-   [<span data-ttu-id="9797d-113">MESinkInvalidated</span><span class="sxs-lookup"><span data-stu-id="9797d-113">MESinkInvalidated</span></span>](mesinkinvalidated.md)

<span data-ttu-id="9797d-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9797d-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9797d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9797d-115">Requirements</span></span>



| <span data-ttu-id="9797d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9797d-116">Requirement</span></span> | <span data-ttu-id="9797d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9797d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9797d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9797d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9797d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9797d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9797d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9797d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9797d-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9797d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9797d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9797d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9797d-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9797d-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9797d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9797d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9797d-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9797d-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9797d-126">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="9797d-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="9797d-127">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="9797d-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="9797d-128">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="9797d-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




