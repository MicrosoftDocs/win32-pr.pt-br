---
description: São usados para definir um endereço MAC (controle de acesso de mídia) do IEEE.
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: DOT11_MAC_ADDRESS (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77b43635462c4b48890599512cc1a413461de72e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828850"
---
# <a name="dot11_mac_address"></a><span data-ttu-id="8b9c1-103">\_Endereço MAC \_ DOT11</span><span class="sxs-lookup"><span data-stu-id="8b9c1-103">DOT11\_MAC\_ADDRESS</span></span>

<span data-ttu-id="8b9c1-104">Os tipos de **\_ \_ endereço MAC DOT11** são usados para definir um endereço MAC (controle de acesso de mídia) do IEEE.</span><span class="sxs-lookup"><span data-stu-id="8b9c1-104">The **DOT11\_MAC\_ADDRESS** types are used to define an IEEE media access control (MAC) address.</span></span>


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="8b9c1-105">**\_Endereço MAC \_ DOT11 \[ 6\]**</span><span class="sxs-lookup"><span data-stu-id="8b9c1-105">**DOT11\_MAC\_ADDRESS\[6\]**</span></span>
</dt> <dd>

<span data-ttu-id="8b9c1-106">Um endereço MAC no formato unicast, multicast ou broadcast.</span><span class="sxs-lookup"><span data-stu-id="8b9c1-106">A MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> <dt>

<span data-ttu-id="8b9c1-107">**\_Endereço MAC do PDOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="8b9c1-107">**PDOT11\_MAC\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="8b9c1-108">Ponteiro para um endereço MAC no formato unicast, multicast ou broadcast.</span><span class="sxs-lookup"><span data-stu-id="8b9c1-108">Pointer to a MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b9c1-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b9c1-109">Requirements</span></span>



| <span data-ttu-id="8b9c1-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b9c1-110">Requirement</span></span> | <span data-ttu-id="8b9c1-111">Valor</span><span class="sxs-lookup"><span data-stu-id="8b9c1-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9c1-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b9c1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8b9c1-113">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="8b9c1-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b9c1-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b9c1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8b9c1-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8b9c1-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8b9c1-116">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="8b9c1-116">Redistributable</span></span><br/>          | <span data-ttu-id="8b9c1-117">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="8b9c1-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="8b9c1-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b9c1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b9c1-119"><dt>Windot11. h (incluir Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b9c1-119"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b9c1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b9c1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b9c1-121">**Lista de DOT11 \_ BSSID \_**</span><span class="sxs-lookup"><span data-stu-id="8b9c1-121">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> <dt>

[<span data-ttu-id="8b9c1-122">**\_atributos de associação de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="8b9c1-122">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="8b9c1-123">**\_entrada de BSS de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="8b9c1-123">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




