---
title: Método GetObjectByTextRepresentation da classe MicrosoftDNS_ResourceRecord
description: O método GetObjectByTextRepresentation recupera uma instância existente da classe MicrosoftDNS \_ ResourceRecord.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- DNS do método GetObjectByTextRepresentation
- Método GetObjectByTextRepresentation DNS, classe MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord classe DNS, método GetObjectByTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455333"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Método GetObjectByTextRepresentation da \_ classe ResourceRecord MicrosoftDNS

O método **GetObjectByTextRepresentation** recupera uma instância existente da classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

## <a name="syntax"></a>Sintaxe


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DnsServerName* \[ no\]
</dt> <dd>

Nome do servidor DNS do qual o RR deve ser recuperado.

</dd> <dt>

*ContainerName* \[ no\]
</dt> <dd>

Nome do contêiner do qual o RR deve ser obtido.

</dd> <dt>

*Textrepresentation* \[ no\]
</dt> <dd>

Representação de texto do RR a ser recuperado.

</dd> <dt>

*RR* \[ fora\]
</dt> <dd>

Referência ao RR instanciado.

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método CreateInstanceFromTextRepresentation da \_ classe ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





