---
title: Método Modify da classe MicrosoftDNS_TXTType
description: O método Modify atualiza um registro de recurso de texto (TXT).
ms.assetid: af61057e-95be-4290-83da-a63f01ead476
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_TXTType classe
- MicrosoftDNS_TXTType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e565d4c48b048b4d72b11c939b644752cb14f1993c2810f127bb14f60bec929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957295"
---
# <a name="modify-method-of-the-microsoftdns_txttype-class"></a>Método Modify da classe MicrosoftDNS \_ TXTType

O método **Modify** atualiza um registro de recurso de texto (txt).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*DescriptiveText* \[ no\]
</dt> <dd>

Texto descritivo, a semântica que depende do domínio do proprietário.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao novo objeto.

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

[**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe TXTType MicrosoftDNS**](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





