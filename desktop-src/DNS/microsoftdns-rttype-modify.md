---
title: Modificar o método da MicrosoftDNS_RTType classe
description: O método Modify atualiza um Registro de Recurso de Rota por (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_RTType classe
- MicrosoftDNS_RTType classe DNS, método Modify
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
ms.openlocfilehash: 2003f8e2840a2684f91a7a01b0341e2e8dcdf0ca88b6bf31fcf58b3a3c6f79bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692396"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a>Modificar método da classe RTType do MicrosoftDNS \_

O **método Modify** atualiza um Registro de Recurso de Rota por (RT).

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

*TTL* \[ in, opcional\]
</dt> <dd>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*Preferência* \[ in, opcional\]
</dt> <dd>

Preferência dada a esse RR entre outros no mesmo proprietário. Valores inferiores são preferenciais.

</dd> <dt>

*IntermediateHost* \[ in, opcional\]
</dt> <dd>

FQDN especificando um host para servir como intermediário para alcançar o host especificado pelo proprietário.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao novo objeto .

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

[**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da classe RTType do MicrosoftDNS \_**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





