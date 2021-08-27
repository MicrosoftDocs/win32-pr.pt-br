---
title: Classe MicrosoftDNS_DomainDomainContainment
description: A \_ classe MicrosoftDNS DomainDomainContainment é usada para contenção de domínio; Os domínios DNS podem conter outros domínios DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- MicrosoftDNS_DomainDomainContainment de classe de DNS
- MicrosoftDNS_DomainDomainContainment de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f96d03f007af463fb4c4f672eb0d1374867636f4a4224469589563b9c5882e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084746"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a>\_Classe MicrosoftDNS DomainDomainContainment

A classe **MicrosoftDNS \_ DomainDomainContainment** é usada para contenção de domínio; Os domínios DNS podem conter outros domínios DNS. Cada instância da classe [**de \_ domínio MicrosoftDNS**](microsoftdns-domain.md) pode conter várias outras instâncias do **\_ domínio MicrosoftDNS**. Uma instância de um objeto de **\_ domínio MicrosoftDNS** está diretamente contida em no máximo um **\_ domínio MicrosoftDNS** de nível superior.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Membros

A classe **MicrosoftDNS \_ DomainDomainContainment** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ DomainDomainContainment** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ domínio MicrosoftDNS**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualificadores: Key, Max (1), Override ("GroupComponent")

Descrição: um domínio, zona, cache ou RootHints de nível superior.

Herdado do \_ componente CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ domínio MicrosoftDNS**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualificadores: chave, substituição ("PartComponent")

Descrição: o domínio contido por um domínio de nível superior, zona, cache ou RootHints.

Herdado do \_ componente CIM.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





