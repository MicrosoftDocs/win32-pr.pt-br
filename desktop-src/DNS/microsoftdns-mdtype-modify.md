---
title: Modificar o método da classe MicrosoftDNS_MDType classe
description: O método Modify atualiza um registro de recurso do MD (Agente de Email para Domínio).
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_MDType classe
- MicrosoftDNS_MDType classe DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c402a753394c5ca7c12acf212377823a87d16e5d17f0d97981ab5e75d8a537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527256"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a>Modificar o método da classe \_ MDType do MicrosoftDNS

O **método Modify** atualiza um registro de recurso do MD (Agente de Email para Domínio).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*MDHost* \[ in, opcional\]
</dt> <dd>

Cadeia de caracteres que representa o host de entrega de email.

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

[**MicrosoftDNS \_ MDType**](microsoftdns-mdtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da classe MDType do MicrosoftDNS \_**](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





