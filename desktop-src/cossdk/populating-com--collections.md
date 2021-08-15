---
description: Populando coleções COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Populando coleções COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256c246a4f5d176e6b706515d02c0dd5cf68f7ae5a9aff7f89949da14510636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990666"
---
# <a name="populating-com-collections"></a>Populando coleções COM+

Depois de recuperar uma coleção e antes de trabalhar diretamente com os itens que ela contém, você deve preencher a coleção usando o método [**populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) . Isso busca dados para o conteúdo da coleção do catálogo COM+.

É importante entender que sempre que você usa os objetos COMAdmin para manipular itens ou dados em coleções, você está realmente trabalhando em dados armazenados em cache transitórios; Você não está trabalhando diretamente com o catálogo persistente. Nada que você faça com uma coleção ou qualquer um de seus itens será refletido no catálogo até que você chame [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) na coleção. Para obter mais detalhes, consulte [salvando ou descartando alterações](saving-or-discarding-changes.md).

Qualquer chamada subsequente para [**popular**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), antes de chamar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), tem o efeito de descartar alterações pendentes para todos os itens na coleção. **Popular** sempre popula o cache no qual você está trabalhando com quaisquer dados que sejam persistidos no armazenamento de dados de catálogo subjacente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Navegando na hierarquia da coleção COM+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Consultando coleções relacionadas disponíveis](querying-for-available-related-collections.md)
</dt> <dt>

[Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



