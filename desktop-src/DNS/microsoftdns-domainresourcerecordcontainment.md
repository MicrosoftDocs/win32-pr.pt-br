---
title: MicrosoftDNS_DomainResourceRecordContainment classe
description: A classe DomainResourceRecordContainment da MicrosoftDNS é usada para contenção de RR; cada instância do Domínio MicrosoftDNS pode conter várias instâncias da \_ \_ classe \_ ResourceRecord do MicrosoftDNS.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- dns MicrosoftDNS_DomainResourceRecordContainment classe
- MicrosoftDNS_DomainResourceRecordContainment classe DNS , descrita
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
ms.openlocfilehash: 498d9b953895ebece94dc77edb587045d1cfdd45c29f04c202756bd1080dc9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795606"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a>Classe \_ DomainResourceRecordContainment do MicrosoftDNS

A **classe \_ DomainResourceRecordContainment da MicrosoftDNS** é usada para contenção de RR; cada instância do [**Domínio MicrosoftDNS \_**](microsoftdns-domain.md) pode conter várias instâncias da [**classe \_ ResourceRecord do MicrosoftDNS.**](microsoftdns-resourcerecord.md) Cada instância da **classe \_ ResourceRecord do MicrosoftDNS** pertence a uma única instância da classe **domínio MicrosoftDNS \_** e é definida como fraca para essa instância.

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

A **classe \_ DomainResourceRecordContainment do MicrosoftDNS** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ DomainResourceRecordContainment da MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Domínio MicrosoftDNS \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualificadores: Key, Override("GroupComponent")

Descrição: a zona, o cache, o RootHints ou o domínio que contém diretamente o Registro de Recurso.

Herdado do \_ componente CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **MicrosoftDNS \_ ResourceRecord**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualificadores: Key, Override("PartComponent")

Descrição: o registro de recurso contido em um Domínio, Zona, Cache ou RootHints.

Herdado do componente \_ CIM.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[**Domínio Do \_ MicrosoftDNSDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





