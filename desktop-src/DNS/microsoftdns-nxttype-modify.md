---
title: Método Modify da classe MicrosoftDNS_NXTType
description: O método Modify atualiza um próximo registro de recurso (NXT).
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_NXTType classe
- MicrosoftDNS_NXTType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bab7bf8480c7e18914cac4f7ae0deb8a608090f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454867"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a>Método Modify da classe MicrosoftDNS \_ NXTType

O método **Modify** atualiza um próximo registro de recurso (NXT).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*NextDomainName* \[ no\]
</dt> <dd>

Próximo nome de domínio.

</dd> <dt>

*Tipos* \[ no\]
</dt> <dd>

Lista separada por espaços dos mnemônicos do tipo RR para o nome do proprietário do registro de recurso NXT.

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

[**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe NXTType MicrosoftDNS**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





