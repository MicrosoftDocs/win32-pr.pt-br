---
title: Modificar o método da MicrosoftDNS_MINFOType classe
description: O método Modify atualiza um Registro de Recurso de Informações de Email (MINFO).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_MINFOType classe
- MicrosoftDNS_MINFOType classe DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954015ffdb01a8655a7762d3c364abe3440a8cfd19ec7eabf5ad8db5cf11c8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692556"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a>Modificar o método da classe \_ MINFOType do MicrosoftDNS

O **método Modify** atualiza um Registro de Recurso de Informações de Email (MINFO).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*ResponsibleMailbox* \[ in, opcional\]
</dt> <dd>

FQDN especificando uma caixa de correio responsável pela lista de correspondência ou caixa de correio especificada no Nome do Proprietário do registro.

</dd> <dt>

*ErrorMailbox* \[ in, opcional\]
</dt> <dd>

FQDN especificando uma caixa de correio para receber mensagens de erro relacionadas à lista de correspondência ou à caixa de correio especificada pelo nome do proprietário do registro MINFO.

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

[**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da classe MINFOType do MicrosoftDNS \_**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





