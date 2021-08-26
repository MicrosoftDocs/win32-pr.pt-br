---
title: Método CreateInstanceFromTextRepresentation da classe MicrosoftDNS_ResourceRecord
description: O método CreateInstanceFromTextRepresentation instancia um objeto MicrosoftDNS \_ ResourceRecord.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- DNS do método CreateInstanceFromTextRepresentation
- Método CreateInstanceFromTextRepresentation DNS, classe MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord classe DNS, método CreateInstanceFromTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8ee7f92db1185fe2762b0b308b4fbafdbdd80e7417c7b615939c72333f15e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104016"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Método CreateInstanceFromTextRepresentation da \_ classe ResourceRecord MicrosoftDNS

O método **CreateInstanceFromTextRepresentation** instancia um objeto [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

## <a name="syntax"></a>Sintaxe


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DnsServerName* \[ no\]
</dt> <dd>

Nome do servidor DNS no qual o RR deve ser criado.

</dd> <dt>

*ContainerName* \[ no\]
</dt> <dd>

Nome do contêiner no qual o novo RR deve ser colocado.

</dd> <dt>

*Textrepresentation* \[ no\]
</dt> <dd>

Representação de texto da instância de RR a ser criada.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao RR instanciado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método GetObjectByTextRepresentation da \_ classe ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





