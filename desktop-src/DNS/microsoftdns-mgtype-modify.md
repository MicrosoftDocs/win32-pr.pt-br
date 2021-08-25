---
title: Modificar o método da MicrosoftDNS_MGType classe
description: O método Modify atualiza um registro de recurso do MG (Grupo de Email).
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_MGType classe
- MicrosoftDNS_MGType classe DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db26f33e56ecc8553af1e34513a085b6eb6666ca99e2f91ec19383756094d6f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874906"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a>Modificar método da classe MGType do MicrosoftDNS \_

O **método Modify** atualiza um registro de recurso do MG (Grupo de Email).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*MGMailbox* \[ in, opcional\]
</dt> <dd>

FQDN especificando uma caixa de correio que seja membro do grupo de email especificado pelo nome do proprietário do registro.

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

[**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da classe MGType do MicrosoftDNS \_**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





