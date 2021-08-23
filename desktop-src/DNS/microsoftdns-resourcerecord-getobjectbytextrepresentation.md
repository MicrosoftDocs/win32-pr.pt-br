---
title: Método GetObjectByTextRepresentation da classe MicrosoftDNS_ResourceRecord
description: O método GetObjectByTextRepresentation recupera uma instância existente da classe \_ ResourceRecord do MicrosoftDNS.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- Método GetObjectByTextRepresentation DNS
- Método DNS GetObjectByTextRepresentation, MicrosoftDNS_ResourceRecord classe
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
ms.openlocfilehash: 08e3b824ccabe86e842d4ef6f61799b33110b5d28a58658a6d4cbedc824c134b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692416"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Método GetObjectByTextRepresentation da classe ResourceRecord do MicrosoftDNS \_

O **método GetObjectByTextRepresentation** recupera uma instância existente da [**classe \_ ResourceRecord do MicrosoftDNS.**](microsoftdns-resourcerecord.md)

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

*DnsServerName* \[ Em\]
</dt> <dd>

Nome do servidor DNS do qual o RR deve ser recuperado.

</dd> <dt>

*ContainerName* \[ Em\]
</dt> <dd>

Nome do contêiner do qual o RR deve ser obtido.

</dd> <dt>

*TextRepresentation* \[ Em\]
</dt> <dd>

Representação de texto do RR a ser recuperado.

</dd> <dt>

*RR* \[ out\]
</dt> <dd>

Referência ao RR instautado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método CreateInstanceFromTextRepresentation da classe ResourceRecord do MicrosoftDNS \_**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





