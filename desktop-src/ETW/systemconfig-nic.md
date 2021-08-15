---
description: Essa classe é a classe de tipo de evento para eventos de configuração de placa de interface de rede. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: SystemConfig_NIC classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 822e8404137eee9731bbfcee9f5d9f4495609078c4251b53269371dd4904cea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393812"
---
# <a name="systemconfig_nic-class"></a>Classe NIC SystemConfig \_

Essa classe é a classe de tipo de evento para eventos de configuração de placa de interface de rede.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a>Membros

A **classe \_ NIC SystemConfig** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ NIC SystemConfig** tem essas propriedades.

<dl> <dt>

DnsServerAddresses
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(7), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Endereços IP a serem usados na consulta para servidores DNS. A lista de endereços é delimitada por vírgulas.

</dd> <dt>

Ipaddresses
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(6), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Endereços IP associados à placa de interface de rede. A lista de endereços é delimitada por vírgulas.

</dd> <dt>

Ipv4Index
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3)
</dt> </dl>

Índice de adaptador para NIC IPv4. O índice do adaptador pode mudar quando um adaptador é desabilitado e habilitado ou em outras circunstâncias e não deve ser considerado persistente.

</dd> <dt>

Ipv6Index
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4)
</dt> </dl>

Índice de adaptador para NIC IPv6. O índice do adaptador pode mudar quando um adaptador é desabilitado e habilitado ou em outras circunstâncias e não deve ser considerado persistente.

</dd> <dt>

NICDescription
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(5), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Descrição do adaptador.

</dd> <dt>

PhysicalAddr
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1), Format("x")
</dt> </dl>

Endereço de hardware para o adaptador.

</dd> <dt>

PhysicalAddrLen
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2)
</dt> </dl>

Comprimento do endereço de hardware para o adaptador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




