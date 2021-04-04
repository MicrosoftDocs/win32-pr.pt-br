---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_SIGType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de assinatura (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21660572d9557e6425b459c5694a7eeee4722cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008989"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a>Método CreateInstanceFromPropertyData da \_ classe SIGType MicrosoftDNS

O método **CreateInstanceFromPropertyData** instancia um registro de recurso de assinatura (SIG).

## <a name="syntax"></a>Sintaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
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

*DnsServerName* \[ no\]
</dt> <dd>

FQDN ou endereço IP do servidor DNS que contém este RR.

</dd> <dt>

*ContainerName* \[ no\]
</dt> <dd>

Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.

</dd> <dt>

*OwnerName* \[ no\]
</dt> <dd>

Nome do proprietário do RR.

</dd> <dt>

*RecordClass* \[ em, opcional\]
</dt> <dd>

Classe do RR. O valor padrão é 1. Os valores a seguir são válidos.



| Valor                                                                                                | Significado                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | NO (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CAOS)<br/>    |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

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
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | Criptografia de curva elíptica<br/> |



 

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

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

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

[**Método Modify da classe MicrosoftDNS \_ SIGType**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





