---
description: Obtendo e definindo propriedades
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Obtendo e definindo propriedades (serviços de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457056"
---
# <a name="getting-and-setting-properties-component-services"></a>Obtendo e definindo propriedades (serviços de componentes)

Antes de ler ou gravar propriedades específicas expostas por um item em uma coleção, você deve executar as seguintes etapas:

1.  Recupere a coleção.
2.  Preencha a coleção para ler os dados do catálogo COM+.
3.  Recupere o item específico na coleção, representando-o com um objeto da classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Para obter um exemplo que ilustra essas etapas, consulte [navegando na hierarquia da coleção com+](navigating-the-com--collection-hierarchy.md).

Porque as propriedades específicas expostas podem variar dependendo do que o item representa; ou seja, um item que representa um componente tem propriedades diferentes de um que representa um aplicativo COM+. Defina qualquer uma dessas propriedades usando uma única propriedade genérica, a propriedade Value, em [**COMAdminCatalogObject**](comadmincatalogobject.md).

A propriedade Value permite que você obtenha ou defina qualquer propriedade nomeada específica exposta por um item, retornando um valor para uma propriedade nomeada ao obter e tomando um nome e um valor ao definir.

No entanto, nenhuma alteração é registrada no catálogo COM+ até que você salve explicitamente as alterações usando o método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . As alterações pendentes para todas as propriedades em todos os itens em uma determinada coleção são salvas de uma só vez. Para obter detalhes, consulte [salvando ou descartando alterações](saving-or-discarding-changes.md).

Nem todas as alterações feitas serão aceitas. O catálogo COM+ impõe alguma lógica de coerência para garantir que você configure as coisas de forma razoável. Além disso, quando você altera algumas propriedades, outras podem ser alteradas automaticamente pela mesma lógica de coerência. Esses efeitos aparecem quando você tenta salvar as alterações.

> [!Note]  
> É possível que você esteja em contenção com outro gravador no catálogo COM+. Entre as chamadas para [**popular**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para uma determinada coleção, você não tem um bloqueio em nenhum desses dados no catálogo. Várias partes podem estar simultaneamente Configurando itens em uma determinada coleção e podem ser contendedas quando salvam alterações. Isso significa que outra pessoa pode alterar as configurações de um objeto antes ou depois de fazer isso, executando algum tipo de programa usando os objetos COMAdmin ou usando a ferramenta administrativa serviços de componentes, seja local ou remotamente. A regra geral com a gravação de objetos no catálogo é que todas as propriedades em um objeto são gravadas ao mesmo tempo. Ou seja, o último gravador vence — o objeto é salvo no catálogo precisamente como o último gravador o configurou.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interdependências entre propriedades](interdependencies-between-properties.md)
</dt> <dt>

[Consultando as propriedades disponíveis](querying-for-available-properties.md)
</dt> <dt>

[Salvando ou descartando alterações](saving-or-discarding-changes.md)
</dt> </dl>

 

 



