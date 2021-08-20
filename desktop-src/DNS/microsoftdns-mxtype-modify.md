---
title: Método Modify da classe MicrosoftDNS_MXType
description: O método Modify atualiza um registro de recurso do servidor de mensagens (MR).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_MXType classe
- MicrosoftDNS_MXType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fb31da6bf0861c94c54163fa9c771ac592fca105a5459214e17031c3b8e6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076780"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a>Método Modify da classe MicrosoftDNS \_ MXType

O método **Modify** atualiza um registro de recurso do servidor de mensagens (Mr).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*Preferência* \[ em, opcional\]
</dt> <dd>

Preferência dada a esse RR entre outros no mesmo proprietário. Os valores mais baixos são preferenciais.

</dd> <dt>

*MailExchange* \[ em, opcional\]
</dt> <dd>

FQDN que especifica um host que está disposto a atuar como uma troca de email para o nome do proprietário.

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

[**MicrosoftDNS \_ MXType**](microsoftdns-mxtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe MXType MicrosoftDNS**](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





