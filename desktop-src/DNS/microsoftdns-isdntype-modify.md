---
title: Método Modify da classe MicrosoftDNS_ISDNType
description: O método Modify atualiza um registro de recurso de ISDN.
ms.assetid: 09e23853-ca92-43a3-8bd9-7de10eb5eddc
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_ISDNType classe
- MicrosoftDNS_ISDNType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c369a6650c834ff9f35af6389c346daec86a954
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918016"
---
# <a name="modify-method-of-the-microsoftdns_isdntype-class"></a>Método Modify da \_ classe isdntype MicrosoftDNS

O método **Modify** atualiza um registro de recurso de ISDN.

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                ISDNNumber,
  [in, optional] string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*ISDNNumber* \[ em, opcional\]
</dt> <dd>

Número ISDN e DDI do proprietário do registro.

</dd> <dt>

*Subendereço* \[ em, opcional\]
</dt> <dd>

Subendereço do proprietário, se definido.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao novo objeto.

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

[**\_Isdntype MicrosoftDNS**](microsoftdns-isdntype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe isdntype MicrosoftDNS**](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





