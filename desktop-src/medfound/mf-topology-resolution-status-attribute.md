---
description: Especifica o status de uma tentativa de resolver uma topologia.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: Atributo MF_TOPOLOGY_RESOLUTION_STATUS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827619"
---
# <a name="mf_topology_resolution_status-attribute"></a><span data-ttu-id="e0c0f-103">\_Atributo de \_ status de resolução de topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="e0c0f-103">MF\_TOPOLOGY\_RESOLUTION\_STATUS attribute</span></span>

<span data-ttu-id="e0c0f-104">Especifica o status de uma tentativa de resolver uma topologia.</span><span class="sxs-lookup"><span data-stu-id="e0c0f-104">Specifies the status of an attempt to resolve a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="e0c0f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e0c0f-105">Data type</span></span>

<span data-ttu-id="e0c0f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e0c0f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e0c0f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0c0f-107">Remarks</span></span>

<span data-ttu-id="e0c0f-108">O carregador de topologia ou a sessão de mídia pode definir esse atributo em uma topologia.</span><span class="sxs-lookup"><span data-stu-id="e0c0f-108">The topology loader or the Media Session might set this attribute on a topology.</span></span> <span data-ttu-id="e0c0f-109">O valor desse atributo é um bit a bit **ou** de sinalizadores da enumeração de sinalizadores de [**status de \_ \_ resolução de \_ \_ topologia MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) .</span><span class="sxs-lookup"><span data-stu-id="e0c0f-109">The value of this attribute is a bitwise **OR** of flags from the [**MF\_TOPOLOGY\_RESOLUTION\_STATUS\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) enumeration.</span></span>

<span data-ttu-id="e0c0f-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e0c0f-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c0f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0c0f-111">Requirements</span></span>



| <span data-ttu-id="e0c0f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0c0f-112">Requirement</span></span> | <span data-ttu-id="e0c0f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e0c0f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c0f-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0c0f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e0c0f-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0c0f-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e0c0f-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0c0f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e0c0f-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e0c0f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e0c0f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0c0f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0c0f-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0c0f-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0c0f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0c0f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0c0f-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0c0f-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e0c0f-122">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e0c0f-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e0c0f-123">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="e0c0f-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e0c0f-124">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="e0c0f-124">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[<span data-ttu-id="e0c0f-125">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="e0c0f-125">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




