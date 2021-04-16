---
description: Contém sinalizadores que definem os recursos da sessão de mídia, com base na apresentação atual.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: Atributo MF_EVENT_SESSIONCAPS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af38d61f07bf038d1906d6f11e46fea63e800efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753881"
---
# <a name="mf_event_sessioncaps-attribute"></a><span data-ttu-id="c1b4e-103">\_Atributo SESSIONCAPS do evento MF \_</span><span class="sxs-lookup"><span data-stu-id="c1b4e-103">MF\_EVENT\_SESSIONCAPS attribute</span></span>

<span data-ttu-id="c1b4e-104">Contém sinalizadores que definem os recursos da sessão de mídia, com base na apresentação atual.</span><span class="sxs-lookup"><span data-stu-id="c1b4e-104">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="c1b4e-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c1b4e-105">Data type</span></span>

<span data-ttu-id="c1b4e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c1b4e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c1b4e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1b4e-107">Remarks</span></span>

<span data-ttu-id="c1b4e-108">Este atributo contém um or **bit a** bit de zero ou mais sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="c1b4e-108">This attribute contains a bitwise **OR** of zero or more flags.</span></span> <span data-ttu-id="c1b4e-109">Para obter uma lista de possíveis sinalizadores, consulte [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="c1b4e-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span>

<span data-ttu-id="c1b4e-110">Esse atributo é usado com o evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="c1b4e-110">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="c1b4e-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c1b4e-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b4e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1b4e-112">Requirements</span></span>



| <span data-ttu-id="c1b4e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1b4e-113">Requirement</span></span> | <span data-ttu-id="c1b4e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c1b4e-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b4e-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1b4e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c1b4e-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1b4e-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c1b4e-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1b4e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c1b4e-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1b4e-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c1b4e-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1b4e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1b4e-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1b4e-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1b4e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1b4e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b4e-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c1b4e-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1b4e-123">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="c1b4e-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1b4e-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c1b4e-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c1b4e-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="c1b4e-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




