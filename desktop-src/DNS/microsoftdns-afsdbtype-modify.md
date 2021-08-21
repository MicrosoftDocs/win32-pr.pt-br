---
title: Modificar o método da classe MicrosoftDNS_AFSDBType classe
description: O método Modify atualiza um Registro de Recurso do AFSDB (Servidor de Banco de Dados do Sistema de Arquivos) Andrew.
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_AFSDBType classe
- MicrosoftDNS_AFSDBType classe DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385b80d853c3b610971803c0b1d80a81b7b7c2335186fe4585e63f60c3e3cca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104056"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a>Modificar o método da classe AfSDBType do MicrosoftDNS \_

O **método Modify** atualiza um Registro de Recurso do AFSDB (Servidor de Banco de Dados do Sistema de Arquivos) Andrew.

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*Subtipo* \[ in, opcional\]
</dt> <dd>

Subtipo do servidor AFS host. Para o subtipo 1 (value=1), o host tem um Servidor de Localização de Volume afS versão 3.0 para a célula afS nomeada. No caso do subtipo 2 (value=2), o host tem um servidor de nomes autenticado que mantém o nó de diretório raiz da célula para a célula DCE/NCA nomeada.

</dd> <dt>

*ServerName* \[ in, opcional\]
</dt> <dd>

FQDN especificando um host que tem um servidor para a célula AFS especificada no nome do proprietário.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao objeto modificado.

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

[**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da classe AfSDBType do MicrosoftDNS \_**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





