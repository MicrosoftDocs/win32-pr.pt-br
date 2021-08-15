---
description: Classe TcpIp_Fail-essa classe é a classe de tipo de evento para eventos de falha de TCP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 1fe20b8c-b8f1-4db0-af78-1ebfc40b2bbd
title: Classe TcpIp_Fail
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_Fail
- TcpIp_Fail.Proto
- TcpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd637db3f509e8c23de764eb82cc35b49cb435a7772a14adbe2954d292696e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814526"
---
# <a name="tcpip_fail-class"></a>Classe de falha de TcpIp \_

Essa classe é a classe de tipo de evento para eventos de falha de TCP/IP.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a>Membros

A classe **tcpip \_ Fail** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **tcpip \_ Fail** tem essas propriedades.

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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IP**](tcpip.md)
</dt> </dl>

 

 




