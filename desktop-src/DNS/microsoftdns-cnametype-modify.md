---
title: Método Modify da classe MicrosoftDNS_CNAMEType
description: O método Modify atualiza um registro de recurso de nome canônico (CNAME).
ms.assetid: 7e550026-d901-44a0-86ac-520682232ccb
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_CNAMEType classe
- MicrosoftDNS_CNAMEType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ddbe1e1592c4331be808340c216954cd8d7b14f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455161"
---
# <a name="modify-method-of-the-microsoftdns_cnametype-class"></a>Método Modify da classe MicrosoftDNS \_ cnametype

O método **Modify** atualiza um registro de recurso de nome CANÔNICO (CNAME).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*Primárioname* \[ em, opcional\]
</dt> <dd>

Cadeia de caracteres que representa o nome primário do registro CNAME.

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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_Cnametype MicrosoftDNS**](microsoftdns-cnametype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe cnametype MicrosoftDNS**](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





