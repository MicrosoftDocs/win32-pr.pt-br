---
title: Classe MicrosoftDNS_ServerDomainContainment
description: Cada instância da \_ classe WMI de associação de servidor MicrosoftDNS pode conter várias instâncias da \_ classe de domínio MicrosoftDNS.
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- MicrosoftDNS_ServerDomainContainment de classe de DNS
- MicrosoftDNS_ServerDomainContainment de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644341"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a>\_Classe MicrosoftDNS ServerDomainContainment

Cada instância da classe WMI de associação de [**\_ servidor MicrosoftDNS**](microsoftdns-server.md) pode conter várias instâncias da classe de [**\_ domínio MicrosoftDNS**](microsoftdns-domain.md) . Cada instância da classe **de \_ domínio MicrosoftDNS** pertence a uma única instância da classe **de \_ servidor MicrosoftDNS** e é definida para ser fraca para esse servidor.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Membros

A classe **MicrosoftDNS \_ ServerDomainContainment** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ ServerDomainContainment** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ servidor MicrosoftDNS**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualificadores: Key, Override ("GroupComponent"), min (1), Max (1)

Descrição: o servidor DNS.

Herdado **do \_ componente CIM**.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ domínio MicrosoftDNS**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualificadores: chave, substituição ("PartComponent")

Descrição: um domínio, zona, cache ou RootHints gerenciado pelo servidor DNS.

Herdado **do \_ componente CIM**.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **MicrosoftDNS \_ ServerDomainContainment** é derivada da classe **de \_ componente CIM** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





