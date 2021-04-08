---
description: Interdependências entre propriedades
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Interdependências entre propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920401"
---
# <a name="interdependencies-between-properties"></a>Interdependências entre propriedades

Quando você define propriedades, o catálogo COM+ impõe alguma lógica de coerência para garantir que você configure elementos de forma razoável. Essa lógica pode ser implementada de duas maneiras, da seguinte maneira:

-   **Depend.** Você pode estar impedido de fazer algumas alterações porque outra propriedade depende de uma configuração específica para uma propriedade que você tentar definir. Por exemplo, se um componente for definido com as transações de atributo necessárias e se você tentar alterar a configuração de sincronização para nenhum, um erro será gerado quando você tentar chamar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) , pois as transações dependem da sincronização.
-   **Efeitos colaterais.** Algumas propriedades podem ser alteradas sem que você as defina explicitamente. Por exemplo, se você definir um componente com as transações de atributo necessárias, a sincronização será definida como obrigatória também. Isso é realmente o lado inverso das dependências — uma propriedade tem precedência sobre outra, e sua dependência é expressa pela primeira configuração da propriedade secundária e, em seguida, pelo bloqueio das alterações nela.

Na lista de propriedades expostas por itens em uma coleção, todos listados em [coleções de administração com+](com--administration-collections.md), as dependências e os efeitos colaterais são declarados para cada propriedade. Ao configurar aplicativos e componentes COM+, você deve estar ciente das restrições que são impostas nas configurações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Obtendo e definindo propriedades](getting-and-setting-properties.md)
</dt> <dt>

[Consultando as propriedades disponíveis](querying-for-available-properties.md)
</dt> <dt>

[Salvando ou descartando alterações](saving-or-discarding-changes.md)
</dt> </dl>

 

 



