---
title: Método Modify da classe MicrosoftDNS_WINSRType
description: O método Modify atualiza um registro de recurso WINSr (pesquisa inversa do WINS).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_WINSRType classe
- MicrosoftDNS_WINSRType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db7865110b0e79642dc91671094c06dfbd10e07cd89684dab58623a9456cca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076660"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a>Método Modify da classe MicrosoftDNS \_ WINSRType

O método **Modify** atualiza um registro de recurso WINSR (pesquisa inversa do WINS).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*MappingFlag* \[ em, opcional\]
</dt> <dd>

Sinalizador de mapeamento WINSr que especifica se o registro deve ser incluído na replicação de zona. Ele pode ter apenas dois valores: 0x80000000 e 0x00010000 correspondentes aos sinalizadores de replicação e sem replicação (registro local), respectivamente.

</dd> <dt>

*LookupTimeout* \[ em, opcional\]
</dt> <dd>

Tempo limite, em segundos, para um servidor DNS usando a pesquisa inversa do WINS.

</dd> <dt>

*CacheTimeout* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, um servidor DNS usando a pesquisa WINS pode armazenar em cache a resposta do servidor WINS.

</dd> <dt>

*ResultDomain* \[ em, opcional\]
</dt> <dd>

Nome de domínio a ser anexado aos nomes NetBIOS retornados.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao novo objeto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

[**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe WINSRType MicrosoftDNS**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





