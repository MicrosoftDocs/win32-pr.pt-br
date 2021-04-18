---
description: Define um tipo de rede de BSS (conjunto de serviços básico).
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: Enumeração de DOT11_BSS_TYPE (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSS_TYPE
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 7815e75f3ef7ef8d908b7d2b26f2e5f9d3630009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759194"
---
# <a name="dot11_bss_type-enumeration"></a><span data-ttu-id="0bbdd-103">\_Enumeração de \_ tipo BSS DOT11</span><span class="sxs-lookup"><span data-stu-id="0bbdd-103">DOT11\_BSS\_TYPE enumeration</span></span>

<span data-ttu-id="0bbdd-104">O tipo de rede de **\_ \_ tipo de BSS DOT11** enumerated define um tipo básico do conjunto de serviços (BSS).</span><span class="sxs-lookup"><span data-stu-id="0bbdd-104">The **DOT11\_BSS\_TYPE** enumerated type defines a basic service set (BSS) network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bbdd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bbdd-105">Syntax</span></span>


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="0bbdd-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0bbdd-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0bbdd-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**\_infraestrutura de \_ tipo \_ BSS dot11**</span><span class="sxs-lookup"><span data-stu-id="0bbdd-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**dot11\_BSS\_type\_infrastructure**</span></span>
</dt> <dd>

<span data-ttu-id="0bbdd-108">Especifica uma rede de BSS de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="0bbdd-108">Specifies an infrastructure BSS network.</span></span>

</dd> <dt>

<span data-ttu-id="0bbdd-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**tipo de BSS de dot11 \_ \_ \_ independente**</span><span class="sxs-lookup"><span data-stu-id="0bbdd-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**dot11\_BSS\_type\_independent**</span></span>
</dt> <dd>

<span data-ttu-id="0bbdd-110">Especifica uma rede BSS (IBSS) independente.</span><span class="sxs-lookup"><span data-stu-id="0bbdd-110">Specifies an independent BSS (IBSS) network.</span></span>

</dd> <dt>

<span data-ttu-id="0bbdd-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**\_tipo de BSS de dot11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bbdd-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11\_BSS\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="0bbdd-112">Especifica a infraestrutura ou a rede IBSS.</span><span class="sxs-lookup"><span data-stu-id="0bbdd-112">Specifies either infrastructure or IBSS network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bbdd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bbdd-113">Requirements</span></span>



| <span data-ttu-id="0bbdd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bbdd-114">Requirement</span></span> | <span data-ttu-id="0bbdd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0bbdd-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbdd-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bbdd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0bbdd-117">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="0bbdd-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0bbdd-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bbdd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0bbdd-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0bbdd-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="0bbdd-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="0bbdd-120">Redistributable</span></span><br/>          | <span data-ttu-id="0bbdd-121">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="0bbdd-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="0bbdd-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0bbdd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bbdd-123"><dt>Wlantypes. h (incluir Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bbdd-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bbdd-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bbdd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bbdd-125">**\_entrada de BSS de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="0bbdd-125">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[<span data-ttu-id="0bbdd-126">**\_parâmetros de conexão WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="0bbdd-126">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="0bbdd-127">**WlanGetNetworkBssList**</span><span class="sxs-lookup"><span data-stu-id="0bbdd-127">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




