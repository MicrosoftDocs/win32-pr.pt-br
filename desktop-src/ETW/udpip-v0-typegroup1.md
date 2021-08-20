---
description: UdpIp_V0_TypeGroup1 classe - essa classe é a classe de tipo de evento para eventos UDP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: UdpIp_V0_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8061009fcf419bd7b5ab04eda0b056a8ccee1ad3f3b990a0846058599f34fbde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813758"
---
# <a name="udpip_v0_typegroup1-class"></a>Classe TypeGroup1 UdpIp \_ V0 \_

Essa classe é a classe de tipo de evento para eventos UDP/IP.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ TypeGroup1 UdpIp V0** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ TypeGroup1 UdpIp V0** tem essas propriedades.

<dl> <dt>

contexto
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1), ponteiro
</dt> </dl>

Identificador de processo para o Objeto de Endereço que fez ou recebeu a solicitação.

</dd> <dt>

paidr
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(5), Extension("IPAddr")
</dt> </dl>

Endereço IP de destino.

</dd> <dt>

Dport
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(6), Extension("Port")
</dt> </dl>

Número da porta de destino.

</dd> <dt>

dsize
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(7)
</dt> </dl>

Tamanho do pacote de destino.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2), Extension("IPAddr")
</dt> </dl>

Endereço IP de origem.

</dd> <dt>

tamanho
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4)
</dt> </dl>

Tamanho do pacote de origem.

</dd> <dt>

Esporte
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3), Extension("Port")
</dt> </dl>

Número da porta de origem.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**UdpIp \_ V0**](udpip-v0.md)
</dt> </dl>

 

 




