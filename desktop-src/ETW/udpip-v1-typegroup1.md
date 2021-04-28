---
description: Classe UdpIp_V1_TypeGroup1-essa classe é a classe de tipo de evento para eventos UDP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: Classe UdpIp_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: d7dadaac3d418d2351f9e27c694309deb373615e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105404"
---
# <a name="udpip_v1_typegroup1-class"></a>\_Classe UdpIp v1 \_ TypeGroup1

Essa classe é a classe de tipo de evento para eventos UDP/IP.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ TypeGroup1 UdpIp v1** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ TypeGroup1 UdpIp v1** tem essas propriedades.

<dl> <dt>

daddr
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3), extensão ("IPAddr")
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

Qualificadores: WmiDataId (4), extensão ("IPAddr")
</dt> </dl>

Endereço IP de origem.

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**UdpIp \_ v1**](udpip-v1.md)
</dt> <dt>

[**UdpIp**](udpip.md)
</dt> </dl>

 

 




