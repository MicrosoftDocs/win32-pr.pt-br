---
title: Método Modify da classe MicrosoftDNS_HINFOType
description: O método Modify atualiza um registro de recurso de informações de host (HINFO).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_HINFOType classe
- MicrosoftDNS_HINFOType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29a01eb94d82d080142d3496bab5f7f0b9acac8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644661"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a>Método Modify da classe MicrosoftDNS \_ HINFOType

O método **Modify** atualiza um registro de recurso de informações de host (HINFO).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*CPU* \[ em, opcional\]
</dt> <dd>

Tipo de CPU do proprietário do registro.

</dd> <dt>

*Sistema operacional* \[ em, opcional\]
</dt> <dd>

Sistema operacional do proprietário do registro.

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

[**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe HINFOType MicrosoftDNS**](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





