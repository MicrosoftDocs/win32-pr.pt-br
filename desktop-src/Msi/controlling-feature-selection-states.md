---
description: Você pode controlar quais opções de instalação de recurso estão disponíveis para que os usuários e aplicativos selecionem criando a tabela de recursos e a tabela de componentes.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Controlando Estados de seleção de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd269e5b7b0c810df6f7f0909d56b98cdd1c54c9b51eacc40656fe48fc32f8e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379901"
---
# <a name="controlling-feature-selection-states"></a>Controlando Estados de seleção de recursos

Você pode controlar quais opções de instalação de recurso estão disponíveis para que os usuários e aplicativos selecionem criando a [tabela de recursos](feature-table.md) e a [tabela de componentes](component-table.md).

-   Para evitar a seleção do estado de anúncio de um recurso, inclua **msidbFeatureAttributesDisallowAdvertise** no campo atributos do recurso na [tabela de recursos](feature-table.md).
-   Para evitar a seleção dos Estados de execução da origem ou execução da rede para um recurso, inclua **msidbComponentAttributesLocalOnly** nos campos de atributos na [tabela de componentes](component-table.md) para cada componente pertencente ao recurso. Se um recurso não tiver componentes, o recurso sempre terá as opções executar-de-origem e executar-de-meu-computador disponíveis.
-   Para evitar a seleção do estado de execução de meu computador para um recurso, inclua **msidbComponentAttributesSourceOnly** nos campos de atributos na [tabela de componentes](component-table.md) para cada componente pertencente ao recurso. Se um recurso não tiver componentes, o recurso sempre terá as opções executar-de-origem e executar-de-meu-computador disponíveis.
-   Novos recursos filho podem ser criados incluindo **msidbFeatureAttributesFollowParent** e **MsidbFeatureAttributesUIDisallowAbsent** no campo atributos da [tabela de recursos](feature-table.md).

 

 



