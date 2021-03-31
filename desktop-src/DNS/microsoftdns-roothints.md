---
title: Classe MicrosoftDNS_RootHints
description: A \_ classe MicrosoftDNS RootHints descreve o RootHints armazenado em um arquivo de cache em um servidor DNS. Essa classe simplifica a visualização da contenção de objetos DNS, em vez de representar um objeto real.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- MicrosoftDNS_RootHints de classe de DNS
- MicrosoftDNS_RootHints de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085715"
---
# <a name="microsoftdns_roothints-class"></a>\_Classe MicrosoftDNS RootHints

A classe **MicrosoftDNS \_ RootHints** descreve o RootHints armazenado em um arquivo de cache em um servidor DNS. Essa classe simplifica a visualização da contenção de objetos DNS, em vez de representar um objeto real.

**MicrosoftDNS \_ RootHints** é um contêiner para os registros de recursos armazenados pelo servidor DNS em um arquivo de cache. Cada instância da classe **MicrosoftDNS \_ RootHints** deve ser atribuída a exatamente um servidor DNS. Ele pode ser associado a várias instâncias da classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Membros

A classe **MicrosoftDNS \_ RootHints** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **MicrosoftDNS \_ RootHints** tem esses métodos.



| Método                        | Descrição                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| **Getdistinguiname**      | Recupera o nome distinto da zona. <br/> Qualificadores: implementados<br/>   |
| **WriteBackRootHintDatafile** | Grava o RootHints de volta no arquivo de cache DNS. <br/> Qualificadores: implementados<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_Domínio MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Método WriteBackRootHintDatafile da \_ classe RootHints MicrosoftDNS**](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[**Método getdistinguiname da classe MicrosoftDNS \_ RootHints**](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





