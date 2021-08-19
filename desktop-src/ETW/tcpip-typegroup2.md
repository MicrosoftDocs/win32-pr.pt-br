---
description: Essa classe é a classe de tipo de evento para IPv4 TCP/IP conectar e aceitar eventos. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: TcpIp_TypeGroup2 classe
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
ms.openlocfilehash: 316daec5b6bb186756f8597a63ee35d18125181b6575ae24c8ba8fae63f53d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814496"
---
# <a name="tcpip_typegroup2-class"></a>Classe TcpIp \_ TypeGroup2

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

A **classe TcpIp \_ TypeGroup2** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ TypeGroup2 TcpIp** tem essas propriedades.

<dl> <dt>

**connid**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(15)**, **Pointer**
</dt> </dl>

Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.

</dd> <dt>

**paidr**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(3)**, **Extension("IPAddrV4")**
</dt> </dl>

Endereço IP de destino.

</dd> <dt>

**Dport**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(5)**, **Extension("Port")**
</dt> </dl>

Número da porta de destino.

</dd> <dt>

**Mss**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(7)**
</dt> </dl>

Tamanho máximo do segmento.

</dd> <dt>

**Pid**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(1)**
</dt> </dl>

Identificador do processo associado à solicitação.

</dd> <dt>

**rcvwin**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(11)**
</dt> </dl>

Tamanho da Janela de Recebimento TCP.

</dd> <dt>

**rcvwinscale**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(12)**
</dt> </dl>

Fator de dimensionamento da janela de recebimento TCP.

</dd> <dt>

**opt**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(8)**
</dt> </dl>

Opção DE CONFIRMAÇÃO Seletiva (JUST) no header TCP.

</dd> <dt>

**saddr**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(4)**, **Extension("IPAddrV4")**
</dt> </dl>

Endereço IP de origem.

</dd> <dt>

**seqnum**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(14)**
</dt> </dl>

Número da sequência.

</dd> <dt>

**size**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(2)**
</dt> </dl>

Tamanho do pacote.

</dd> <dt>

**sndwinscale**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(13)**
</dt> </dl>

Fator de dimensionamento da janela de envio de TCP.

</dd> <dt>

**Esporte**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(6)**, **Extension("Port")**
</dt> </dl>

Número da porta de origem.

</dd> <dt>

**tsopt**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(9)**
</dt> </dl>

Opção carimbo de data/hora no header TCP.

</dd> <dt>

**wsopt**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId(10)**
</dt> </dl>

Opção De escala de janela no header TCP.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tcpip**](tcpip.md)
</dt> </dl>

 

 




