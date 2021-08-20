---
title: MicrosoftDNS_Domain classe
description: A classe domínio MicrosoftDNS \_ representa um domínio em uma hierarquia DNS.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- dns MicrosoftDNS_Domain classe
- MicrosoftDNS_Domain classe DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a30b171777e6c8a99ddadcfb39c8cdfdd90b09a43ae255c9bbcc026db09bdb1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163314"
---
# <a name="microsoftdns_domain-class"></a>Classe de domínio MicrosoftDNS \_

A **classe domínio MicrosoftDNS \_** representa um domínio em uma hierarquia DNS.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a>Membros

A **classe \_ domínio MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ domínio MicrosoftDNS** tem esses métodos.



| Método                   | Descrição                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| **GetDistinguishedName** | Obtém o nome diferenciado de DS para a zona. <br/> Qualificadores: implementados<br/> |



 

### <a name="properties"></a>Propriedades

A **classe \_ domínio MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**Containername**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do contêiner do domínio, que pode ser uma Zona, Cache ou RootHints.

Nos casos em que o Contêiner é uma Zona (uma instância da classe [**Zona MicrosoftDNS), \_**](microsoftdns-zone.md) essa propriedade contém o FQDN da Zona.

Quando o Contêiner é a zona raiz, a cadeia de caracteres \\ . \\ deve ser usada.

Nos casos em que o Contêiner é o cache DNS dos registros de recursos (uma instância da classe [**Cache \_ MicrosoftDNS),**](microsoftdns-cache.md) essa propriedade é definida como a cadeia de caracteres \\ .. Cache \\ .

Se o Contêiner for RootHints (uma instância da [**classe \_ RootHints do MicrosoftDNS),**](microsoftdns-roothints.md) essa propriedade deverá ser definida como \\ .. RootHints \\ .

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN ou endereço IP do Servidor DNS que contém o domínio.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN do domínio.

Para instâncias de Cache DNS ou RootHints, as cadeias de caracteres \\ .. Cache \\ e \\ .. RootHints \\ deve ser usado, respectivamente.

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

[**Método GetDistinguishedName da classe de domínio \_ MicrosoftDNS**](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





