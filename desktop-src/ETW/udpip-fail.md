---
description: Classe UdpIp_Fail-essa classe é a classe de tipo de evento para eventos de falha de TCP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 552e63ef-70e4-4bc4-be33-bd77bd5acd61
title: Classe UdpIp_Fail
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_Fail
- UdpIp_Fail.Proto
- UdpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: f923f26e1371d11e27bfd58bcb69c053bfb5f1a3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105504"
---
# <a name="udpip_fail-class"></a>\_Classe UdpIp Fail

Essa classe é a classe de tipo de evento para eventos de falha de TCP/IP.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class UdpIp_Fail : UdpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a>Membros

A classe **UdpIp \_ Fail** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **UdpIp \_ Fail** tem essas propriedades.

<dl> <dt>

**FailureCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Motivo da falha. Pode ser um dos seguintes códigos:

<dl> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**Erro \_ do \_Recursos INsuficientes** (1)
</dt> <dt>

<span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**Erro \_ do Excesso \_ de \_ endereços** (2)
</dt> <dt>

<span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**Erro \_ do O endereço \_ existe** (3)
</dt> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Erro \_ do \_Endereço inválido** (4)
</dt> <dt>

<span id="ERROR_OTHER"></span><span id="error_other"></span>**Erro \_ do OUTRO** (5)
</dt> <dt>

<span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**Erro \_ do O endereço de espera \_ \_ existe** (6)
</dt> </dl>

</dd> <dt>

**Proto**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica o protocolo. Pode ser um dos seguintes valores:



| Valor                                                                                                                                                                                                  | Significado                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>     | A família de endereços IPv4 (protocolo IP versão 4).<br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl> | A família de endereços IPv6 (protocolo IP versão 6).<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**UdpIp**](udpip.md)
</dt> </dl>

 

 




