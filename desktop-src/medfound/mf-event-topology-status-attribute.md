---
description: Especifica o status de uma topologia durante a reprodução.
ms.assetid: f7c93bad-1a64-45b0-ab5c-6edea4a1c0d1
title: Atributo MF_EVENT_TOPOLOGY_STATUS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3c6e00722239103058ca584ee1da28778511c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781540"
---
# <a name="mf_event_topology_status-attribute"></a><span data-ttu-id="c19b8-103">\_Atributo de \_ status da topologia de evento MF \_</span><span class="sxs-lookup"><span data-stu-id="c19b8-103">MF\_EVENT\_TOPOLOGY\_STATUS attribute</span></span>

<span data-ttu-id="c19b8-104">Especifica o status de uma topologia durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="c19b8-104">Specifies the status of a topology during playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="c19b8-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c19b8-105">Data type</span></span>

<span data-ttu-id="c19b8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c19b8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c19b8-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c19b8-107">Remarks</span></span>

<span data-ttu-id="c19b8-108">O valor desse atributo é um membro da enumeração [**MF \_ TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) .</span><span class="sxs-lookup"><span data-stu-id="c19b8-108">The value of this attribute is a member of the [**MF\_TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) enumeration.</span></span>

<span data-ttu-id="c19b8-109">Esse atributo é usado com o evento [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="c19b8-109">This attribute is used with the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

<span data-ttu-id="c19b8-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c19b8-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c19b8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c19b8-111">Requirements</span></span>



| <span data-ttu-id="c19b8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c19b8-112">Requirement</span></span> | <span data-ttu-id="c19b8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c19b8-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c19b8-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c19b8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c19b8-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c19b8-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c19b8-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c19b8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c19b8-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c19b8-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c19b8-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c19b8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c19b8-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c19b8-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c19b8-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c19b8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c19b8-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c19b8-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c19b8-122">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="c19b8-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="c19b8-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c19b8-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c19b8-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="c19b8-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




