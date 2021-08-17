---
description: Essa classe é a classe de tipo de evento para eventos de configuração de placa de interface de rede.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: Classe SystemConfig_V0_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6abe9356ce222d8f461509ec9cfa25ab0a49b8583022ee5e1d832cf29a226dcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746466"
---
# <a name="systemconfig_v0_nic-class"></a>\_ \_ Classe NIC SystemConfig V0

Essa classe é a classe de tipo de evento para eventos de configuração de placa de interface de rede.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ NIC SystemConfig V0** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ NIC SystemConfig V0** tem essas propriedades.

<dl> <dt>

**Dados**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (16)
</dt> </dl>

Campo de dados.

</dd> <dt>

**DhcpServer**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (8)
</dt> </dl>

Endereço IP do servidor de protocolo DHCP. Um valor de 255.255.255.255 indica que o servidor DHCP não pôde ser acessado ou está em processo de ser atingido. Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4). O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.

</dd> <dt>

**DnsServer1**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (12)
</dt> </dl>

Primeiro endereços IP do servidor a serem usados na consulta de servidores DNS. Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4). O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.

</dd> <dt>

**DnsServer2**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (13)
</dt> </dl>

O segundo endereço IP do servidor a ser usado na consulta de servidores DNS. Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4). O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.

</dd> <dt>

**DnsServer3**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (14)
</dt> </dl>

Os endereços IP do terceiro servidor a serem usados na consulta de servidores DNS. Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4). O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.

</dd> <dt>

**DnsServer4**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (15)
</dt> </dl>

Quarto endereço IP do servidor a ser usado na consulta de servidores DNS. Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4). O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.

</dd> <dt>

**Gateway**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (9)
</dt> </dl>

Endereço IP do gateway padrão que o sistema de computador usa. Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4). O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (2)
</dt> </dl>

Índice do adaptador. O índice do adaptador pode ser alterado quando um adaptador está desabilitado e, em seguida, habilitado ou em outras circunstâncias, e não deve ser considerado persistente.

</dd> <dt>

**IP**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (6)
</dt> </dl>

Endereços IP associados à placa de interface de rede. Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4). O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.

</dd> <dt>

**NICName**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (1), **Max** (256)
</dt> </dl>

Nome da placa de interface de rede.

</dd> <dt>

**PhysicalAddr**
</dt> <dd> <dl> <dt>

Tipo de dados: **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (4), **máx** . (8)
</dt> </dl>

Endereço de hardware do adaptador.

</dd> <dt>

**PhysicalAddrLen**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (3)
</dt> </dl>

Comprimento do endereço de hardware para o adaptador.

</dd> <dt>

**PrimaryWinsServer**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (10)
</dt> </dl>

Endereço IP do servidor WINS primário. Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4). O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.

</dd> <dt>

**SecondaryWinsServer**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (11)
</dt> </dl>

Endereço IP do servidor WINS secundário. Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4). O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.

</dd> <dt>

**Tamanho**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (5)
</dt> </dl>

Tamanho, em bytes, da propriedade Data.

</dd> <dt>

**SubnetMask**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (7)
</dt> </dl>

Máscara de sub-rede associada à placa de interface de rede. Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4). O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




