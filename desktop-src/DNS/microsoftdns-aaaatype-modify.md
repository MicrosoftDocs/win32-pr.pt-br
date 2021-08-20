---
title: Modificar o método da classe MicrosoftDNS_AAAAType dados
description: O método Modify atualiza um registro de recurso de endereço IPv6 (AAAA).
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_AAAAType classe
- MicrosoftDNS_AAAAType classe DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417275b9e5fdf1c499f34fd49af3c40f8e208d43673a5d53dc9ba4c3b1ef2c95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967396"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a>Modificar o método da classe \_ MicrosoftDNS AAAAType

O **método Modify** atualiza um registro de recurso de endereço IPv6 (AAAA).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*IPv6Address* \[ in, opcional\]
</dt> <dd>

Endereço IPv6 para o host.

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

[**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da classe \_ MicrosoftDNS AAAAType**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





