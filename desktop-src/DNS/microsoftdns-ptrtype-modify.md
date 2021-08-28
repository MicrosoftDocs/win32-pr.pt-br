---
title: Método Modify da classe MicrosoftDNS_PTRType
description: O método Modify atualiza um registro de recurso de ponteiro (PTR).
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_PTRType classe
- MicrosoftDNS_PTRType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbda85610e34fa6208bac5f8b9ba196be1b24fcadf8a53d87cea627718e9bd04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432816"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a>Método Modify da classe MicrosoftDNS \_ PTRType

O método **Modify** atualiza um registro de recurso de ponteiro (PTR).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*PTRDomainName* \[ em, opcional\]
</dt> <dd>

Endereço do nome de domínio do registro PTR.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao objeto modificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

[**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe PTRType MicrosoftDNS**](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





