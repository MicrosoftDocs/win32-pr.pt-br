---
title: Método Modify da classe MicrosoftDNS_SIGType
description: O método Modify atualiza um RR de assinatura (SIG).
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_SIGType classe
- MicrosoftDNS_SIGType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be64eb494eb72ace437aeade8d7d01a6675f99b2b44c4fa461a8e60c8ed3de1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692276"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a>Método Modify da classe MicrosoftDNS \_ SIGType

O método **Modify** atualiza um RR de assinatura (SIG).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*TypeCovered* \[ no\]
</dt> <dd>

Tipo de RR coberto por essa SIG.

</dd> <dt>

*Algoritmo* \[ do no\]
</dt> <dd>

Algoritmo usado com a chave especificada no registro de recurso. Os valores atribuídos são mostrados na tabela a seguir.



| Valor                                                                                                | Significado                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Criptografia de curva elíptica<br/> |



 

</dd> <dt>

*Rótulos* \[ no\]
</dt> <dd>

Contagem não assinada de rótulos no nome do proprietário do RR SIG original. A contagem não inclui o rótulo nulo para a raiz nem qualquer caractere curinga inicial.

</dd> <dt>

*OriginalTTL* \[ no\]
</dt> <dd>

TTL do conjunto de RRs assinado pelo SIG.

</dd> <dt>

*SignatureExpiration* \[ no\]
</dt> <dd>

Data de expiração da assinatura, expressa em segundos desde o início de 1º de janeiro de 1970, hora de Greenwich (GMT), excluindo segundos bissextos.

</dd> <dt>

*SignatureInception* \[ no\]
</dt> <dd>

Data e hora em que a assinatura se torna válida, expressa em segundos desde o início de 1º de janeiro de 1970, Greenwich Mean Time (GMT), excluindo segundos bissextos.

</dd> <dt>

*Keytag* \[ no\]
</dt> <dd>

Método usado para escolher uma chave que verifica um SIG. Consulte RFC 2535, Apêndice C para o método usado para calcular um KeyTag.

</dd> <dt>

*Signatárioname* \[ no\]
</dt> <dd>

Nome de domínio do signatário que gerou o RR SIG.

</dd> <dt>

*Assinatura* \[ do no\]
</dt> <dd>

Assinatura, representada na base 64, formatada conforme definido na RFC 2535, apêndice A.

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

[**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe SIGType MicrosoftDNS**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





