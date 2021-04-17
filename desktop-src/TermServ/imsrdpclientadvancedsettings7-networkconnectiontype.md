---
title: Propriedade IMsRdpClientAdvancedSettings7 NetworkConnectionType
description: Obtém ou define o tipo de conexão de rede usado entre o cliente e o servidor. As informações do tipo de conexão de rede passadas para o servidor ajudam o servidor a ajustar vários parâmetros com base no tipo de conexão de rede.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade NetworkConnectionType
- Propriedade NetworkConnectionType Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade NetworkConnectionType
- Propriedade NetworkConnectionType Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade NetworkConnectionType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782880"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a><span data-ttu-id="4bc28-109">Propriedade IMsRdpClientAdvancedSettings7:: NetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="4bc28-109">IMsRdpClientAdvancedSettings7::NetworkConnectionType property</span></span>

<span data-ttu-id="4bc28-110">Obtém ou define o tipo de conexão de rede usado entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="4bc28-110">Gets or sets the type of network connection used between the client and server.</span></span> <span data-ttu-id="4bc28-111">As informações do tipo de conexão de rede passadas para o servidor ajudam o servidor a ajustar vários parâmetros com base no tipo de conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="4bc28-111">The network connection type information passed on to the server helps the server tune several parameters based on the network connection type.</span></span>

<span data-ttu-id="4bc28-112">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4bc28-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc28-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bc28-113">Syntax</span></span>


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a><span data-ttu-id="4bc28-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4bc28-114">Property value</span></span>

<span data-ttu-id="4bc28-115">O tipo de conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="4bc28-115">The network connection type.</span></span>

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span data-ttu-id="4bc28-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Conexão \_ do Digite \_ modem** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="4bc28-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**CONNECTION\_TYPE\_MODEM** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="4bc28-117">Modem (56 Kbps)</span><span class="sxs-lookup"><span data-stu-id="4bc28-117">Modem (56 Kbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span data-ttu-id="4bc28-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Conexão \_ do \_Banda larga \_ de tipo baixa** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="4bc28-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**CONNECTION\_TYPE\_BROADBAND\_LOW** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="4bc28-119">Banda larga de baixa velocidade (256 kbps a 2 Mbps)</span><span class="sxs-lookup"><span data-stu-id="4bc28-119">Low-speed broadband (256 Kbps to 2 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span data-ttu-id="4bc28-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Conexão \_ do TIPO \_ satélite** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="4bc28-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**CONNECTION\_TYPE\_SATELLITE** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="4bc28-121">Satélite (2 Mbps a 16 Mbps, com alta latência)</span><span class="sxs-lookup"><span data-stu-id="4bc28-121">Satellite (2 Mbps to 16 Mbps, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span data-ttu-id="4bc28-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Conexão \_ do \_Banda larga \_ de tipo alta** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="4bc28-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**CONNECTION\_TYPE\_BROADBAND\_HIGH** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="4bc28-123">Banda larga de alta velocidade (2 Mbps a 10 Mbps)</span><span class="sxs-lookup"><span data-stu-id="4bc28-123">High-speed broadband (2 Mbps to 10 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span data-ttu-id="4bc28-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Conexão \_ do Digite \_ Wan** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="4bc28-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**CONNECTION\_TYPE\_WAN** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="4bc28-125">WAN (rede de longa distância) (10 Mbps ou superior, com alta latência)</span><span class="sxs-lookup"><span data-stu-id="4bc28-125">Wide area network (WAN) (10 Mbps or higher, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span data-ttu-id="4bc28-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Conexão \_ do TIPO \_ LAN** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="4bc28-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**CONNECTION\_TYPE\_LAN** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="4bc28-127">LAN (rede local) (10 Mbps ou superior)</span><span class="sxs-lookup"><span data-stu-id="4bc28-127">Local area network (LAN) (10 Mbps or higher)</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bc28-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bc28-128">Requirements</span></span>



| <span data-ttu-id="4bc28-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bc28-129">Requirement</span></span> | <span data-ttu-id="4bc28-130">Valor</span><span class="sxs-lookup"><span data-stu-id="4bc28-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bc28-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4bc28-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4bc28-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4bc28-132">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="4bc28-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4bc28-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4bc28-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4bc28-134">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="4bc28-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4bc28-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="4bc28-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bc28-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4bc28-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4bc28-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bc28-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bc28-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4bc28-139">IID</span><span class="sxs-lookup"><span data-stu-id="4bc28-139">IID</span></span><br/>                      | <span data-ttu-id="4bc28-140">IID \_ IMsRdpClientAdvancedSettings7 é definido como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="4bc28-140">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bc28-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="4bc28-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc28-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4bc28-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4bc28-143">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4bc28-143">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





