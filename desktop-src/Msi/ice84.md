---
description: ICE84 verifica a tabela AdvtExecuteSequence, a tabela AdminExecuteSequence e a tabela InstallExecuteSequence para verificar se as seguintes ações padrão não foram definidas com condições no campo condição.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297204"
---
# <a name="ice84"></a>ICE84

ICE84 verifica a tabela [AdvtExecuteSequence](advtexecutesequence-table.md), a [tabela AdminExecuteSequence](adminexecutesequence-table.md)e a [tabela InstallExecuteSequence](installexecutesequence-table.md) para verificar se as seguintes [ações padrão](standard-actions.md) não foram definidas com condições no campo condição.

-   [Ação CostInitialize](costinitialize-action.md)
-   [Ação CostFinalize](costfinalize-action.md)
-   [Ação de custo de](filecost-action.md)
-   [Ação InstallValidate](installvalidate-action.md)
-   [Ação InstallInitialize](installinitialize-action.md)
-   [Ação InstallFinalize](installfinalize-action.md)
-   [Ação ProcessComponents](processcomponents-action.md)
-   [Ação PublishFeatures](publishfeatures-action.md)
-   [Ação PublishProduct](publishproduct-action.md)
-   [Ação RegisterProduct](registerproduct-action.md)
-   [Ação UnpublishFeatures](unpublishfeatures-action.md)

Se condições forem encontradas, o ICE84 lançará um aviso.

## <a name="result"></a>Resultado

ICE84 posta o aviso a seguir.



| Erro de ICE84                                                             | Descrição                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| A ação ' \[ 1 \] ' encontrada na tabela% s é uma ação necessária com uma condição. | Uma ação necessária foi criada com uma condição. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



