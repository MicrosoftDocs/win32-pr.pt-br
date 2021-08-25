---
title: MicrosoftDNS_RootHints classe
description: A classe RootHints do MicrosoftDNS \_ descreve o RootHints armazenado em um arquivo cache em um servidor DNS. Essa classe simplifica a visualização da contenção de objetos DNS, em vez de representar um objeto real.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- dns MicrosoftDNS_RootHints classe
- MicrosoftDNS_RootHints classe DNS , descrita
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
ms.openlocfilehash: 050da9acb1d3865fb490035b6de57fcc1279a45b6f9d78c57df305993d590c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912996"
---
# <a name="microsoftdns_roothints-class"></a>Classe RootHints do MicrosoftDNS \_

A **classe \_ RootHints do MicrosoftDNS** descreve o RootHints armazenado em um arquivo cache em um servidor DNS. Essa classe simplifica a visualização da contenção de objetos DNS, em vez de representar um objeto real.

**MicrosoftDNS \_ RootHints** é um contêiner para os registros de recursos armazenados pelo servidor DNS em um arquivo de cache. Cada instância da classe **\_ RootHints do MicrosoftDNS** deve ser atribuída a exatamente um servidor DNS. Ele pode estar associado a várias instâncias da [**classe \_ ResourceRecord do MicrosoftDNS.**](microsoftdns-resourcerecord.md)

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Membros

A **classe \_ RootHints do MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **classe \_ RootHints do MicrosoftDNS** tem esses métodos.



| Método                        | Descrição                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| **GetDistinguishedName**      | Recupera o nome diferenciado para a zona. <br/> Qualificadores: implementados<br/>   |
| **WriteBackRootHintDatafile** | Grava o RootHints de volta no arquivo de Cache DNS. <br/> Qualificadores: implementados<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Domínio \_ MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Método WriteBackRootHintDatafile da classe \_ RootHints do MicrosoftDNS**](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[**Método GetDistinguishedName da classe RootHints do MicrosoftDNS \_**](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





