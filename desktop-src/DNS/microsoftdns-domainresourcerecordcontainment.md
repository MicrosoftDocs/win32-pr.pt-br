---
title: Classe MicrosoftDNS_DomainResourceRecordContainment
description: A \_ classe MicrosoftDNS DomainResourceRecordContainment é usada para confinamento de RR; cada instância do \_ domínio MicrosoftDNS pode conter várias instâncias da \_ classe MicrosoftDNS ResourceRecord.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- MicrosoftDNS_DomainResourceRecordContainment de classe de DNS
- MicrosoftDNS_DomainResourceRecordContainment de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455159"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a>\_Classe MicrosoftDNS DomainResourceRecordContainment

A classe **MicrosoftDNS \_ DomainResourceRecordContainment** é usada para confinamento de RR; cada instância [**do \_ domínio MicrosoftDNS**](microsoftdns-domain.md) pode conter várias instâncias da classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) . Cada instância da classe **MicrosoftDNS \_ ResourceRecord** pertence a uma única instância da classe de **\_ domínio MicrosoftDNS** e é definida para ser fraca para essa instância.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a>Membros

A classe **MicrosoftDNS \_ DomainResourceRecordContainment** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ DomainResourceRecordContainment** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ domínio MicrosoftDNS**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualificadores: chave, substituição ("GroupComponent")

Descrição: a zona, o cache, o RootHints ou o domínio que contém diretamente o registro de recurso.

Herdado do \_ componente CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **MicrosoftDNS \_ ResourceRecord**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualificadores: chave, substituição ("PartComponent")

Descrição: o registro de recurso contido em um domínio, zona, cache ou RootHints.

Herdado do \_ componente CIM.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





