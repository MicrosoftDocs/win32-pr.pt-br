---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de email.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Propriedades de email (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759330"
---
# <a name="email-properties"></a><span data-ttu-id="d301d-103">Propriedades de email</span><span class="sxs-lookup"><span data-stu-id="d301d-103">Email Properties</span></span>

<span data-ttu-id="d301d-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de email.</span><span class="sxs-lookup"><span data-stu-id="d301d-104">Windows Portable Devices supports the following email properties.</span></span>



| <span data-ttu-id="d301d-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d301d-105">Property</span></span>                         | <span data-ttu-id="d301d-106">VarType</span><span class="sxs-lookup"><span data-stu-id="d301d-106">VarType</span></span>        | <span data-ttu-id="d301d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d301d-107">Description</span></span>                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d301d-108">**\_ \_ linha Cco de email WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d301d-108">**WPD\_EMAIL\_BCC\_LINE**</span></span>        | <span data-ttu-id="d301d-109">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="d301d-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d301d-110">Os destinatários Cco da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d301d-110">The BCC recipients of the e-mail message.</span></span> <span data-ttu-id="d301d-111">Os destinatários Cco recebem uma cópia do email, mas seus nomes não são exibidos como destinatários.</span><span class="sxs-lookup"><span data-stu-id="d301d-111">BCC recipients receive a copy of the e-mail, but their names are not displayed as recipients.</span></span>   |
| <span data-ttu-id="d301d-112">**\_ \_ linha CC de email WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d301d-112">**WPD\_EMAIL\_CC\_LINE**</span></span>         | <span data-ttu-id="d301d-113">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="d301d-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d301d-114">Os destinatários CC da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d301d-114">The CC recipients of the e-mail message.</span></span> <span data-ttu-id="d301d-115">Os destinatários de CC recebem uma cópia da mensagem de email e seus nomes são exibidos como destinatários.</span><span class="sxs-lookup"><span data-stu-id="d301d-115">CC recipients receive a copy of the e-mail message, and their names are displayed as recipients.</span></span> |
| <span data-ttu-id="d301d-116">**o \_ email WPD \_ tem \_ anexos**</span><span class="sxs-lookup"><span data-stu-id="d301d-116">**WPD\_EMAIL\_HAS\_ATTACHMENTS**</span></span> | <span data-ttu-id="d301d-117">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="d301d-117">**VT\_BOOL**</span></span>   | <span data-ttu-id="d301d-118">Um valor booliano que especifica se esta mensagem de email tem anexos.</span><span class="sxs-lookup"><span data-stu-id="d301d-118">A Boolean value that specifies whether this e-mail message has attachments.</span></span>                                                               |
| <span data-ttu-id="d301d-119">**o \_ email WPD foi \_ \_ \_ lido**</span><span class="sxs-lookup"><span data-stu-id="d301d-119">**WPD\_EMAIL\_HAS\_BEEN\_READ**</span></span>  | <span data-ttu-id="d301d-120">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="d301d-120">**VT\_BOOL**</span></span>   | <span data-ttu-id="d301d-121">Um valor booliano que especifica se esta mensagem de email foi lida.</span><span class="sxs-lookup"><span data-stu-id="d301d-121">A Boolean value that specifies whether this e-mail message has been read.</span></span>                                                                 |
| <span data-ttu-id="d301d-122">**\_tempo de \_ recebimento de email WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d301d-122">**WPD\_EMAIL\_RECEIVED\_TIME**</span></span>   | <span data-ttu-id="d301d-123">**Data de VT \_**</span><span class="sxs-lookup"><span data-stu-id="d301d-123">**VT\_DATE**</span></span>   | <span data-ttu-id="d301d-124">Um valor que especifica quando a mensagem de email foi recebida.</span><span class="sxs-lookup"><span data-stu-id="d301d-124">A value that specifies when the e-mail message was received.</span></span>                                                                              |
| <span data-ttu-id="d301d-125">**\_endereço de \_ remetente de email WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d301d-125">**WPD\_EMAIL\_SENDER\_ADDRESS**</span></span>  | <span data-ttu-id="d301d-126">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="d301d-126">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d301d-127">O endereço de email do remetente.</span><span class="sxs-lookup"><span data-stu-id="d301d-127">The e-mail address of the sender.</span></span>                                                                                                         |
| <span data-ttu-id="d301d-128">**\_email WPD \_ para \_ linha**</span><span class="sxs-lookup"><span data-stu-id="d301d-128">**WPD\_EMAIL\_TO\_LINE**</span></span>         | <span data-ttu-id="d301d-129">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="d301d-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d301d-130">Os principais destinatários da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d301d-130">The main recipients of the e-mail message.</span></span>                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="d301d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d301d-131">Requirements</span></span>



| <span data-ttu-id="d301d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d301d-132">Requirement</span></span> | <span data-ttu-id="d301d-133">Valor</span><span class="sxs-lookup"><span data-stu-id="d301d-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d301d-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d301d-134">Header</span></span><br/> | <dl> <span data-ttu-id="d301d-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d301d-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d301d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="d301d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d301d-137">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="d301d-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




