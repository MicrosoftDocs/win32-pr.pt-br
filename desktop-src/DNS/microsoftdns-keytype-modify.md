---
title: Modificar o método da MicrosoftDNS_KEYType classe
description: O método Modify atualiza um registro de recurso KEY.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_KEYType classe
- MicrosoftDNS_KEYType classe DNS, método Modify
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
ms.openlocfilehash: ff5b657e940716a7afa2113dcbdc6836ab3680c1dfe37b88a454d9bdd0c7bc28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163251"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a>Modificar o método da classe KEYType MicrosoftDNS \_

O **método Modify** atualiza um registro de recurso KEY.

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

*TTL* \[ in, opcional\]
</dt> <dd>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*Sinalizadores* \[ in, opcional\]
</dt> <dd>

Sinalizadores usados para especificar o mapeamento, conforme descrito em IETF RFC 2535.

</dd> <dt>

*Protocolo* \[ in, opcional\]
</dt> <dd>

Protocolo para o qual a chave especificada no RR pode ser usada. Os valores atribuídos são mostrados na tabela a seguir.



| Valor                                                                                                    | Significado                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | Email<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>     | Dnssec<br/>        |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | Todos os protocolos<br/> |



 

</dd> <dt>

*Algoritmo* \[ in, opcional\]
</dt> <dd>

Algoritmo usado com a chave especificada no registro de recurso. Os valores atribuídos são mostrados na tabela a seguir.



| Valor                                                                                                | Significado                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Criptografia de curva elíptica<br/> |



 

</dd> <dt>

*PublicKey* \[ in, opcional\]
</dt> <dd>

Chave pública, representada na base 64, conforme descrito no Apêndice A do RFC 2535.

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

[**MicrosoftDNS \_ KEYType**](microsoftdns-keytype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da classe KEYType do MicrosoftDNS \_**](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





