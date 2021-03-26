---
description: Essa classe é a classe de tipo de evento para IPv4 TCP/IP conectar e aceitar eventos. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: Classe TcpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 398b6b0e2b7e4684481f13f73bdd94ef4cd76829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502378"
---
# <a name="tcpip_typegroup2-class"></a>\_Classe tcpip TypeGroup2

Essa classe é a classe de tipo de evento para IPv4 TCP/IP conectar e aceitar eventos.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>Membros

A classe **tcpip \_ TypeGroup2** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **tcpip \_ TypeGroup2** tem essas propriedades.

<dl> <dt>

**CONNID**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (15)**, **ponteiro**
</dt> </dl>

Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.

</dd> <dt>

**daddr**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (3)**, **extensão ("IPAddrV4")**
</dt> </dl>

Endereço IP de destino.

</dd> <dt>

**dport**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (5)**, **extensão ("porta")**
</dt> </dl>

Número da porta de destino.

</dd> <dt>

**MSS**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (7)**
</dt> </dl>

Tamanho máximo do segmento.

</dd> <dt>

**PESSOAL**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (1)**
</dt> </dl>

Identificador do processo associado à solicitação.

</dd> <dt>

**rcvwin**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (11)**
</dt> </dl>

Tamanho da janela de recepção TCP.

</dd> <dt>

**rcvwinscale**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (12)**
</dt> </dl>

Fator de dimensionamento da janela de recepção TCP.

</dd> <dt>

**sackopt**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (8)**
</dt> </dl>

Opção SACK (confirmação seletiva) no cabeçalho TCP.

</dd> <dt>

**saddr**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (4)**, **extensão ("IPAddrV4")**
</dt> </dl>

Endereço IP de origem.

</dd> <dt>

**seqnum**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (14)**
</dt> </dl>

Número de sequência.

</dd> <dt>

**size**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (2)**
</dt> </dl>

Tamanho do pacote.

</dd> <dt>

**sndwinscale**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (13)**
</dt> </dl>

Fator de dimensionamento da janela de envio TCP.

</dd> <dt>

**esporte**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (6)**, **extensão ("porta")**
</dt> </dl>

Número da porta de origem.

</dd> <dt>

**tsopt**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (9)**
</dt> </dl>

Opção de carimbo de data/hora no cabeçalho TCP.

</dd> <dt>

**wsopt**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId (10)**
</dt> </dl>

Opção de escala da janela no cabeçalho TCP.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IP**](tcpip.md)
</dt> </dl>

 

 




