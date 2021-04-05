---
title: Método Modify da classe MicrosoftDNS_KEYType
description: O método Modify atualiza um registro de recurso de chave.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_KEYType classe
- MicrosoftDNS_KEYType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ee9182925f3f1d53fb90a4beefeb421f01c24f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086371"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a>Método Modify da \_ classe KeyType MicrosoftDNS

O método **Modify** atualiza um registro de recurso de chave.

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*Sinalizadores* \[ de em, opcional\]
</dt> <dd>

Sinalizadores usados para especificar o mapeamento, conforme descrito em IETF RFC 2535.

</dd> <dt>

*Protocolo* \[ do em, opcional\]
</dt> <dd>

Protocolo para o qual a chave especificada no RR pode ser usada. Os valores atribuídos são mostrados na tabela a seguir.



| Valor                                                                                                    | Significado                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | Email<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>     | DNSSEC<br/>        |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | Todos os protocolos<br/> |



 

</dd> <dt>

*Algoritmo* \[ do em, opcional\]
</dt> <dd>

Algoritmo usado com a chave especificada no registro de recurso. Os valores atribuídos são mostrados na tabela a seguir.



| Valor                                                                                                | Significado                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | Criptografia de curva elíptica<br/> |



 

</dd> <dt>

*PublicKey* \[ em, opcional\]
</dt> <dd>

Chave pública, representada na base 64, conforme descrito no apêndice A de RFC 2535.

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

[**KeyType MicrosoftDNS \_**](microsoftdns-keytype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe KeyType MicrosoftDNS**](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





