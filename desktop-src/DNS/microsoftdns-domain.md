---
title: Classe MicrosoftDNS_Domain
description: A \_ classe de domínio MicrosoftDNS representa um domínio em uma hierarquia de DNS.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- MicrosoftDNS_Domain de classe de DNS
- MicrosoftDNS_Domain de classe de DNS, descrita
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
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085565"
---
# <a name="microsoftdns_domain-class"></a>\_Classe de domínio MicrosoftDNS

A classe de **\_ domínio MicrosoftDNS** representa um domínio em uma hierarquia de DNS.

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

A classe de **\_ domínio MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe de **\_ domínio MicrosoftDNS** tem esses métodos.



| Método                   | Descrição                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| **Getdistinguiname** | Obtém o nome distinto do DS para a zona. <br/> Qualificadores: implementados<br/> |



 

### <a name="properties"></a>Propriedades

A classe de **\_ domínio MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do contêiner do domínio, que pode ser uma zona, um cache ou um RootHints.

Nos casos em que o contêiner é uma zona (uma instância da classe de [**\_ zona MicrosoftDNS**](microsoftdns-zone.md) ), essa propriedade contém o FQDN da zona.

Quando o contêiner é a zona raiz, a cadeia de caracteres \\ \\ deve ser usada.

Nos casos em que o contêiner é o cache DNS dos registros de recursos (uma instância da classe de [**\_ cache MicrosoftDNS**](microsoftdns-cache.md) ), essa propriedade é definida como a cadeia de caracteres \\ . Cache \\ .

Se o contêiner for RootHints (uma instância da classe [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md) ), essa propriedade deverá ser definida como \\ .. RootHints \\ .

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN ou endereço IP do servidor DNS que contém o domínio.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN do domínio.

Para instâncias do cache DNS ou RootHints, as cadeias de caracteres \\ .. Cache \\ e \\ .. RootHints \\ deve ser usado, respectivamente.

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

[**Método getdistinguiname da classe de \_ domínio MicrosoftDNS**](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





