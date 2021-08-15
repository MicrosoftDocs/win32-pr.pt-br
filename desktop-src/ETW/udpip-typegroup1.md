---
description: Essa classe é a classe de tipo de evento para eventos de envio e recebimento UDP/IP IPv4. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: f04e0b4c-6a2b-4452-9bdf-38c08b487863
title: UdpIp_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup1
- UdpIp_TypeGroup1.PID
- UdpIp_TypeGroup1.size
- UdpIp_TypeGroup1.daddr
- UdpIp_TypeGroup1.saddr
- UdpIp_TypeGroup1.dport
- UdpIp_TypeGroup1.sport
- UdpIp_TypeGroup1.seqnum
- UdpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: d7a34d459cd4d9cefc4abbf08a97367309b4d90b31c63148159f57fccf6646c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393645"
---
# <a name="udpip_typegroup1-class"></a>Classe \_ TypeGroup1 UdpIp

Essa classe é a classe de tipo de evento para eventos de envio e recebimento UDP/IP IPv4.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{10, 11}, EventTypeName{"SendIPV4", "RecvIPV4"}]
class UdpIp_TypeGroup1 : UdpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>Membros

A **classe \_ TypeGroup1 UdpIp** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ TypeGroup1 UdpIp** tem essas propriedades.

<dl> <dt>

connid
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(8), Pointer
</dt> </dl>

Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.

</dd> <dt>

paidr
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3), Extension("IPAddrV4")
</dt> </dl>

Endereço IP de destino.

</dd> <dt>

Dport
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(5), Extension("Port")
</dt> </dl>

Número da porta de destino.

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1)
</dt> </dl>

Identificador do processo associado à solicitação.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4), Extension("IPAddrV4")
</dt> </dl>

Endereço IP de origem.

</dd> <dt>

seqnum
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(7)
</dt> </dl>

Número da sequência.

</dd> <dt>

tamanho
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2)
</dt> </dl>

Tamanho do pacote.

</dd> <dt>

Esporte
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(6), Extension("Port")
</dt> </dl>

Número da porta de origem.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**UdpIp**](udpip.md)
</dt> </dl>

 

 




