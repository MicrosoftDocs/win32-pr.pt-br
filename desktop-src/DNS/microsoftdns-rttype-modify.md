---
title: Método Modify da classe MicrosoftDNS_RTType
description: O método Modify atualiza um registro de recurso de rota a (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_RTType classe
- MicrosoftDNS_RTType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8267bf1dc256ec95a456978643226ab5c01af93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499428"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a>Método Modify da classe MicrosoftDNS \_ RTType

O método **Modify** atualiza um registro de recurso de rota a (RT).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
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

*IntermediateHost* \[ em, opcional\]
</dt> <dd>

FQDN que especifica um host para servir como intermediário para atingir o host especificado pelo proprietário.

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

[**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe RTType MicrosoftDNS**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





