---
description: A ação PublishFeatures grava o estado de cada recurso no registro do sistema.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Ação PublishFeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759210"
---
# <a name="publishfeatures-action"></a>Ação PublishFeatures

A ação PublishFeatures grava o estado de cada recurso no registro do sistema. O estado do recurso pode estar ausente, anunciado ou instalado. A ação PublishFeatures também grava o mapeamento de componente de recurso no registro do sistema para cada recurso instalado.

A ação PublishFeatures consulta a tabela [FeatureComponents](featurecomponents-table.md), a [tabela de recursos](feature-table.md)e a tabela de [componentes](component-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação PublishFeatures deve vir antes de [PublishProduct](publishproduct-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação        |
|-------|-----------------------------------|
| \[1\] | Identificador do recurso anunciado. |



 

## <a name="remarks"></a>Comentários

A ação PublishFeatures publica a composição de todos os recursos selecionados para serem anunciados ou instalados.

 

 



