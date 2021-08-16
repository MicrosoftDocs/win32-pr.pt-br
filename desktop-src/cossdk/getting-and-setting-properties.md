---
description: Obter e definir propriedades
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Obter e definir propriedades (Serviços de Componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805d98463e1f9b8f08c1018b49554c95e2735bfa7ea6dca21d90243eb324df49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306751"
---
# <a name="getting-and-setting-properties-component-services"></a>Obter e definir propriedades (Serviços de Componentes)

Antes de ler ou gravar propriedades específicas expostas por um item em uma coleção, você deve seguir as seguintes etapas:

1.  Recupere a coleção.
2.  Preencha a coleção para ler dados para ela no catálogo COM+.
3.  Recupere o item específico na coleção, representando-o com um objeto da [**classe COMAdminCatalogObject.**](comadmincatalogobject.md)

Para ver um exemplo que ilustra essas etapas, consulte [Navegando na Hierarquia de Coleção COM+.](navigating-the-com--collection-hierarchy.md)

Como as propriedades específicas expostas podem variar dependendo do que o item representa; ou seja, um item que representa um componente tem propriedades diferentes de uma que representa um aplicativo COM+. De definir qualquer uma dessas propriedades usando uma única propriedade genérica, a propriedade Value, [**em COMAdminCatalogObject**](comadmincatalogobject.md).

A propriedade Value permite obter ou definir qualquer propriedade nomeada específica exposta por um item, retornando um valor para uma propriedade nomeada ao obter e recebendo um nome e um valor ao definir.

Nenhuma alteração é registrada no catálogo COM+ até que você salve explicitamente as alterações usando o método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) [**no objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md) Alterações pendentes para todas as propriedades em todos os itens em uma determinada coleção são salvas de uma só vez. Para obter detalhes, consulte [Salvando ou descartando alterações](saving-or-discarding-changes.md).

Nem todas as alterações feitas serão aceitas. O catálogo COM+ impõe alguma lógica de coerência para garantir que você configure as coisas de maneira razoável. Além disso, quando você altera algumas propriedades, outras podem mudar automaticamente pela mesma lógica de coerência. Esses efeitos aparecem quando você tenta salvar as alterações.

> [!Note]  
> É possível que você fique em contenção com outro autor no catálogo COM+. Entre chamadas [**para Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) [**e SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para uma determinada coleção, você não tem um bloqueio em nenhum desses dados no catálogo. Várias partes podem configurar simultaneamente itens em uma determinada coleção e podem estar contenção quando salvam alterações. Isso significa que outra pessoa pode alterar as configurações em um objeto antes ou depois de você, executando algum tipo de programa usando os objetos COMAdmin ou usando a ferramenta administrativa dos Serviços de Componentes, localmente ou remotamente. A regra geral com a escrita de objetos no catálogo é que todas as propriedades em um objeto são escritas ao mesmo tempo. Ou seja, o último autor vence– o objeto é salvo no catálogo exatamente como o último autor o configurou.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interdependências entre propriedades](interdependencies-between-properties.md)
</dt> <dt>

[Consultando propriedades disponíveis](querying-for-available-properties.md)
</dt> <dt>

[Salvando ou descartando alterações](saving-or-discarding-changes.md)
</dt> </dl>

 

 



