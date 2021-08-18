---
title: Modificar o método da MicrosoftDNS_RPType classe
description: O método Modify atualiza um registro de recurso rp (pessoa responsável).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_RPType classe
- MicrosoftDNS_RPType classe DNS, método Modify
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
ms.openlocfilehash: 5d237879b883e21c3c6289542e4eae7b9703be64931af788f042b6cdbec2ca49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587486"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a>Modificar o método da classe RPType do MicrosoftDNS \_

O **método Modify** atualiza um registro de recurso rp (pessoa responsável).

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

*TTL* \[ in, opcional\]
</dt> <dd>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*RPMailbox* \[ in, opcional\]
</dt> <dd>

FQDN especificando a caixa de correio do responsável.

</dd> <dt>

*TXTDomainName* \[ in, opcional\]
</dt> <dd>

FQDN para o qual existem registros de recursos TXT.

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

[**RpType do MicrosoftDNS \_**](microsoftdns-rptype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da classe RPType do MicrosoftDNS \_**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





