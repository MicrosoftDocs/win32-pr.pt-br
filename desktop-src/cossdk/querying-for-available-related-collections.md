---
description: Consultando coleções relacionadas disponíveis
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Consultando coleções relacionadas disponíveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296113"
---
# <a name="querying-for-available-related-collections"></a>Consultando coleções relacionadas disponíveis

Se você estiver escrevendo uma ferramenta de administração de finalidade geral, é provável que você precise escrever rotinas para navegar pela hierarquia de coleção inteira. Para dar suporte a isso, o COM+ tem um recurso que permite que você consulte dinamicamente as coleções relacionadas que estão disponíveis em qualquer coleção específica.

A coleção [**RelatedCollectionInfo**](relatedcollectioninfo.md) está disponível em qualquer coleção que você esteja mantendo e contém um item para cada coleção relacionada disponível. Você pode enumerar esses itens para determinar se uma determinada coleção está disponível.

Você pode obter a coleção [**RelatedCollectionInfo**](relatedcollectioninfo.md) de qualquer coleção que estiver mantendo usando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , deixando o segundo parâmetro em branco, em que você normalmente especificaria a propriedade de chave de um item pai.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Navegando na hierarquia da coleção COM+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Populando coleções COM+](populating-com--collections.md)
</dt> <dt>

[Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



