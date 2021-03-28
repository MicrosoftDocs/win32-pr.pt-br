---
description: Essa classe é a classe de tipo de evento para eventos UDP/IP IPv6 Send e Receive. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 059041f6-bf34-4bf8-8e1a-2dfbc6c30edc
title: Classe UdpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup2
- UdpIp_TypeGroup2.PID
- UdpIp_TypeGroup2.size
- UdpIp_TypeGroup2.daddr
- UdpIp_TypeGroup2.saddr
- UdpIp_TypeGroup2.dport
- UdpIp_TypeGroup2.sport
- UdpIp_TypeGroup2.seqnum
- UdpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 88d9cb4935d005f3c25f1fb6c3c421328fb285bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967729"
---
# <a name="udpip_typegroup2-class"></a>\_Classe UdpIp TypeGroup2

Essa classe é a classe de tipo de evento para eventos UDP/IP IPv6 Send e Receive.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{26, 27}, EventTypeName{"SendIPV6", "RecvIPV6"}]
class UdpIp_TypeGroup2 : UdpIp
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

A classe **UdpIp \_ TypeGroup2** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **UdpIp \_ TypeGroup2** tem essas propriedades.

<dl> <dt>

CONNID
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (8), ponteiro
</dt> </dl>

Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.

</dd> <dt>

daddr
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3), extensão ("IPAddrV6")
</dt> </dl>

Endereço IP de destino.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (5), extensão ("porta")
</dt> </dl>

Número da porta de destino.

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1)
</dt> </dl>

Identificador do processo associado à solicitação.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4), extensão ("IPAddrV6")
</dt> </dl>

Endereço IP de origem.

</dd> <dt>

seqnum
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (7)
</dt> </dl>

Número de sequência.

</dd> <dt>

tamanho
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2)
</dt> </dl>

Tamanho do pacote.

</dd> <dt>

esporte
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (6), extensão ("porta")
</dt> </dl>

Número da porta de origem.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**UdpIp**](udpip.md)
</dt> </dl>

 

 




