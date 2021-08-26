---
description: Aqui está um exemplo de uma tabela de sequência.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Exemplo detalhado da tabela de sequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc6e9715850d05231080cd8cd832ac7f39c1e3044628bb307afb51bf92c2210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040186"
---
# <a name="sequence-table-detailed-example"></a>Exemplo detalhado da tabela de sequência

Aqui está um exemplo de uma tabela de sequência.



| Ação                                          | Condição                                                       | Sequência |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [LaunchConditions](launchconditions-action.md) |                                                                 |          |
| [AppSearch](appsearch-action.md)               |                                                                 | 200      |
| [CCPSearch](ccpsearch-action.md)               | teste do CCP \_                                                       | 300      |
| CCPDialog                                       | Não \_ êxito de CCP \_                                               | 400      |
| MyCustomConfig                                  | Não [ **instalado**](installed.md)                              | 500      |
| [CostInitialize](costinitialize-action.md)     |                                                                 | 600      |
| [Custo de](filecost-action.md)                 |                                                                 | 700      |
| [CostFinalize](costfinalize-action.md)         |                                                                 | 800      |
| InstallDialog                                   | Não [ **instalado**](installed.md)                              | 900      |
| MaintenanceDialog                               | [**Instalado**](installed.md) E não [ **retomar**](resume.md) | 1000     |
| ActionDialog                                    |                                                                 | 1100     |
| [RegisterProduct](registerproduct-action.md)   |                                                                 | 1200     |
| [InstallValidate](installvalidate-action.md)   |                                                                 | 1300     |
| [InstallFiles](installfiles-action.md)         |                                                                 | 1.400     |
| Mycustomizable                                  | $MyComponent > 2                                             | 1500     |
| [InstallFinalize](installfinalize-action.md)   |                                                                 | 1600     |



 

As seguintes ações nessa tabela de sequência são definidas pelo instalador e são exemplos de ações padrão:

[LaunchConditions](launchconditions-action.md)

 

[AppSearch](appsearch-action.md)

 

[CCPSearch](ccpsearch-action.md)

 

[CostInitialize](costinitialize-action.md)

 

[Custo de](filecost-action.md)

 

[CostFinalize](costfinalize-action.md)

 

[RegisterProduct](registerproduct-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallValidate](installvalidate-action.md)

As ações a seguir foram definidas pelo autor da tabela e são exemplos de [ações personalizadas](custom-actions.md) e devem ser listadas na [tabela CustomAction](customaction-table.md):

MyCustomConfig

 

Mycustomizable

As entradas restantes no campo de ação são chaves estrangeiras na [tabela de diálogo](dialog-table.md). Eles especificam os nomes das caixas de diálogo que serão exibidas se o campo condição for avaliado como verdadeiro.

CCPDialog

 

InstallDialog

 

MaintenanceDialog

 

ActionDialog

A coluna condição faz com que o instalador ignore a ação se a propriedade ou expressão nesse campo for false. A propriedade [**installed**](installed.md) e a propriedade [**resume**](resume.md) são exemplos de propriedades que são definidas pelo instalador. A propriedade [**installed**](installed.md) será definida como true se o produto já estiver instalado e a propriedade [**resume**](resume.md) for definida se o retomar uma instalação suspensa. O teste do CCP \_ e as \_ Propriedades de êxito not CCP \_ são exemplos de propriedades que podem ser definidas na linha de comando pelo usuário que está instalando o aplicativo.

Todas as ações são executadas em sequência com as seguintes etapas condicionais:

-   O CPPSearch será executado somente se o \_ teste do CCP estiver definido.
-   CCPDialog será executado somente se o \_ êxito de CCP não \_ for definido.
-   MaintenanceDialog será executado somente se este produto já estiver instalado e se não for uma instalação que está sendo retomada após ser suspensa.
-   MyCustomAction será executado somente se a expressão na coluna Condition for true. A expressão $MyComponent > 2 refere-se ao estado de ação do componente chamado myComponent. Essa condição indica que mycustomizable deve ser executada somente se myComponent estiver definido para ser instalado. Para obter mais informações sobre Estados de ação e Estados de seleção, consulte a propriedade [**FeatureRequestState**](session-featurerequeststate.md) , a [tabela de recursos](feature-table.md)e a [ação InstallFiles](installfiles-action.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando propriedades](using-properties.md)
</dt> <dt>

[Sintaxe de instrução condicional](conditional-statement-syntax.md)
</dt> </dl>

 

 



