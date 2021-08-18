---
title: Modificar o método da classe MicrosoftDNS_AType
description: O método Modify atualiza o TTL e o endereço IP de um registro de recurso de endereço de host (A).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_AType classe
- MicrosoftDNS_AType classe DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d9f4740aeec92726796943e53b4d2143a6378341b061aaa7d3f3f6bf6dc7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163477"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a>Modificar método da classe \_ MicrosoftDNS AType

O **método Modify** atualiza o TTL e o endereço IP de um registro de recurso de endereço de host (A).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*IPAddress* \[ in, opcional\]
</dt> <dd>

Cadeia de caracteres que representa o endereço IP do host.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao objeto modificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Qualquer parâmetro não especificado é deixado inalterado no registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da classe \_ MicrosoftDNS AType**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





