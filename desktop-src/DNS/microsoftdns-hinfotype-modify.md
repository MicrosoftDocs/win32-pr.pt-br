---
title: Modificar o método da MicrosoftDNS_HINFOType classe
description: O método Modify atualiza um registro de recurso de informações do host (HINFO).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_HINFOType classe
- MicrosoftDNS_HINFOType classe DNS, método Modify
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
ms.openlocfilehash: 344177f0e0a18da22294faef24a6d1c4e61598b4b5e8a804081bdd3a592cf440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984636"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a>Modificar o método da classe HINFOType do MicrosoftDNS \_

O **método Modify** atualiza um registro de recurso de informações do host (HINFO).

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

*TTL* \[ in, opcional\]
</dt> <dd>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*CPU* \[ in, opcional\]
</dt> <dd>

Tipo de CPU do proprietário do registro.

</dd> <dt>

*SISTEMA OPERACIONAL* \[ in, opcional\]
</dt> <dd>

Sistema operacional do proprietário do registro.

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

[**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da classe HINFOType do MicrosoftDNS \_**](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





