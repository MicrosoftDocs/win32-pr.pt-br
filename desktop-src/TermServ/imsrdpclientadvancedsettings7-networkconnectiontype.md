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
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a>Propriedade IMsRdpClientAdvancedSettings7:: NetworkConnectionType

Obtém ou define o tipo de conexão de rede usado entre o cliente e o servidor. As informações do tipo de conexão de rede passadas para o servidor ajudam o servidor a ajustar vários parâmetros com base no tipo de conexão de rede.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a>Valor da propriedade

O tipo de conexão de rede.

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Conexão \_ do Digite \_ modem** (1 (0x1))


</dt> <dd>

Modem (56 Kbps)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Conexão \_ do \_Banda larga \_ de tipo baixa** (2 (0x2))


</dt> <dd>

Banda larga de baixa velocidade (256 kbps a 2 Mbps)

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Conexão \_ do TIPO \_ satélite** (3 (0x3))


</dt> <dd>

Satélite (2 Mbps a 16 Mbps, com alta latência)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Conexão \_ do \_Banda larga \_ de tipo alta** (4 (0x4))


</dt> <dd>

Banda larga de alta velocidade (2 Mbps a 10 Mbps)

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Conexão \_ do Digite \_ Wan** (5 (0x5))


</dt> <dd>

WAN (rede de longa distância) (10 Mbps ou superior, com alta latência)

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Conexão \_ do TIPO \_ LAN** (6 (0x6))


</dt> <dd>

LAN (rede local) (10 Mbps ou superior)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 é definido como 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





