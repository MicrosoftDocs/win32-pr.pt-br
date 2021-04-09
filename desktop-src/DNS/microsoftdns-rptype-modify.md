---
title: Método Modify da classe MicrosoftDNS_RPType
description: O método Modify atualiza um registro de recurso de pessoa responsável (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_RPType classe
- MicrosoftDNS_RPType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ec575424e6e26c79f8d6a27e62732cad6ddc57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824505"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a>Método Modify da classe MicrosoftDNS \_ RPType

O método **Modify** atualiza um registro de recurso de pessoa responsável (RP).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*RPMailbox* \[ em, opcional\]
</dt> <dd>

FQDN que especifica a caixa de correio da pessoa responsável.

</dd> <dt>

*TXTDomainName* \[ em, opcional\]
</dt> <dd>

FQDN para o qual os registros de recurso TXT existem.

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

[**MicrosoftDNS \_ RPType**](microsoftdns-rptype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe RPType MicrosoftDNS**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





