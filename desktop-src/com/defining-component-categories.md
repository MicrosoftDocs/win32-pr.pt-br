---
title: Definindo categorias de componentes
description: Definindo categorias de componentes
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160492"
---
# <a name="defining-component-categories"></a>Definindo categorias de componentes

O autor de uma definição de categoria de componente cria um GUID exclusivo (o CATID) que é publicado junto com a definição. Outras partes conhecem a definição desse tipo e podem fazer uso de suas classes com suporte de acordo. Como a assinatura do método de uma interface, a semântica de uma categoria não deve ser modificada após ser instalada. É melhor manter a compatibilidade com versões anteriores da categoria, introduzindo um novo identificador de categoria com semântica revisada.

Como os identificadores de interface (IID) e os identificadores de categoria de componente (CATID) existem em namespaces diferentes, parece que seria possível usar o mesmo GUID para um IID e um CATID. No entanto, como IIDs geralmente são usados para o CLSID do servidor proxy/stub da interface, há o potencial de conflito. Portanto, não use o mesmo GUID para um IID e o CATID.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associando ícones a uma categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizando por recursos de componente](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorizando por recursos de contêiner](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classes e associações padrão](default-classes-and-associations.md)
</dt> <dt>

[O Gerenciador de categorias de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




