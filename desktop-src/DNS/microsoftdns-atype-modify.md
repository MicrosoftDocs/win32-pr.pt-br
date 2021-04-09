---
title: Método Modify da classe MicrosoftDNS_AType
description: O método Modify atualiza o TTL e o endereço IP de um registro de recurso de endereço de host (A).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_AType classe
- MicrosoftDNS_AType classe de DNS, método Modify
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
ms.openlocfilehash: 2ffda093ed843cfd655711100321c9876120519c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009379"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a>Método Modify da classe MicrosoftDNS \_ AType

O método **Modify** atualiza o TTL e o endereço IP de um registro de recurso de endereço de host (a).

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

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*IPAddress* \[ em, opcional\]
</dt> <dd>

Cadeia de caracteres que representa o endereço IP do host.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao objeto modificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Qualquer parâmetro não especificado permanece inalterado no registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe AType MicrosoftDNS**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





