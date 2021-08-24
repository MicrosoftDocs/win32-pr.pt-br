---
title: Método Modify da classe MicrosoftDNS_SOAType
description: O método Modify atualiza um registro de recurso de início de autoridade (SOA).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_SOAType classe
- MicrosoftDNS_SOAType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74785804ebed8266443f0dd708a5d122e350a6cf88b91f228d2ce266481dffaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825076"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a>Método Modify da classe MicrosoftDNS \_ SOAType

O método **Modify** atualiza um registro de recurso de início de autoridade (SOA).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*SerialNumber* \[ em, opcional\]
</dt> <dd>

O número de série SOA que representa o número de vezes que a zona foi atualizada, usada pelos [*servidores secundários*](s-gly.md) para determinar se a transferência de zona é necessária.

</dd> <dt>

*PrimaryServer* \[ em, opcional\]
</dt> <dd>

Nome do servidor primário.

</dd> <dt>

*ResponsibleParty* \[ em, opcional\]
</dt> <dd>

Endereço da caixa de correio da parte responsável, na forma de alias. Domain, como xyz.microsoft.com. Observe o uso de um período em vez de um símbolo de arroba (@).

</dd> <dt>

*RefreshInterval* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, antes que a zona que contém esse registro deve ser atualizada.

</dd> <dt>

*RetryDelay* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, o servidor DNS deve atrasar entre as tentativas de resolução de nome.

</dd> <dt>

*ExpireLimit* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que os servidores secundários devem aguardar por uma resposta do servidor primário antes de descartar suas cópias do arquivo de zona como inválidas.

</dd> <dt>

*MinimumTTL* \[ em, opcional\]
</dt> <dd>

Tempo de vida útil, em segundos, aplicado aos registros de recursos na zona que não especificam seu próprio TTL.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao objeto modificado

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

[**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





