---
description: Contém o SSID de uma interface.
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: Estrutura de DOT11_SSID (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_SSID
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: e319d22db33a627be631f9b6b0ee36591bc7a5bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828846"
---
# <a name="dot11_ssid-structure"></a><span data-ttu-id="09042-103">\_Estrutura DOT11 SSID</span><span class="sxs-lookup"><span data-stu-id="09042-103">DOT11\_SSID structure</span></span>

<span data-ttu-id="09042-104">Uma estrutura **DOT11 \_ SSID** contém o SSID de uma interface.</span><span class="sxs-lookup"><span data-stu-id="09042-104">A **DOT11\_SSID** structure contains the SSID of an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="09042-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09042-105">Syntax</span></span>


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a><span data-ttu-id="09042-106">Membros</span><span class="sxs-lookup"><span data-stu-id="09042-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="09042-107">**uSSIDLength**</span><span class="sxs-lookup"><span data-stu-id="09042-107">**uSSIDLength**</span></span>
</dt> <dd>

<span data-ttu-id="09042-108">O comprimento, em bytes, da matriz **ucSSID** .</span><span class="sxs-lookup"><span data-stu-id="09042-108">The length, in bytes, of the **ucSSID** array.</span></span>

</dd> <dt>

<span data-ttu-id="09042-109">**ucSSID**</span><span class="sxs-lookup"><span data-stu-id="09042-109">**ucSSID**</span></span>
</dt> <dd>

<span data-ttu-id="09042-110">O SSID.</span><span class="sxs-lookup"><span data-stu-id="09042-110">The SSID.</span></span> <span data-ttu-id="09042-111">O \_ \_ comprimento máximo \_ de DOT11 SSID é definido como 32.</span><span class="sxs-lookup"><span data-stu-id="09042-111">DOT11\_SSID\_MAX\_LENGTH is set to 32.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09042-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="09042-112">Remarks</span></span>

<span data-ttu-id="09042-113">O SSID especificado pelo membro **ucSSID** não é uma cadeia de caracteres ASCII terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="09042-113">The SSID that is specified by the **ucSSID** member is not a null-terminated ASCII string.</span></span> <span data-ttu-id="09042-114">O comprimento do SSID é determinado pelo membro **uSSIDLength** .</span><span class="sxs-lookup"><span data-stu-id="09042-114">The length of the SSID is determined by the **uSSIDLength** member.</span></span>

<span data-ttu-id="09042-115">Um SSID curinga é um SSID cujo membro **uSSIDLength** está definido como zero.</span><span class="sxs-lookup"><span data-stu-id="09042-115">A wildcard SSID is an SSID whose **uSSIDLength** member is set to zero.</span></span> <span data-ttu-id="09042-116">Quando o SSID desejado é definido como o caractere curinga SSID, a estação 802,11 pode se conectar a qualquer rede de BSS (conjunto de serviços) básica.</span><span class="sxs-lookup"><span data-stu-id="09042-116">When the desired SSID is set to the wildcard SSID, the 802.11 station can connect to any basic service set (BSS) network.</span></span>

## <a name="requirements"></a><span data-ttu-id="09042-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09042-117">Requirements</span></span>



| <span data-ttu-id="09042-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="09042-118">Requirement</span></span> | <span data-ttu-id="09042-119">Valor</span><span class="sxs-lookup"><span data-stu-id="09042-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09042-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09042-120">Minimum supported client</span></span><br/> | <span data-ttu-id="09042-121">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="09042-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="09042-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09042-122">Minimum supported server</span></span><br/> | <span data-ttu-id="09042-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09042-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="09042-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="09042-124">Redistributable</span></span><br/>          | <span data-ttu-id="09042-125">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="09042-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="09042-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09042-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="09042-127"><dt>Wlantypes. h (incluir Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09042-127"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09042-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="09042-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09042-129">**\_parâmetros de conexão WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="09042-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="09042-130">**WlanGetNetworkBssList**</span><span class="sxs-lookup"><span data-stu-id="09042-130">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[<span data-ttu-id="09042-131">**WlanScan**</span><span class="sxs-lookup"><span data-stu-id="09042-131">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




