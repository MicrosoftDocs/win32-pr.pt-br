---
description: Consultando propriedades disponíveis
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Consultando propriedades disponíveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f41278e6f7ee5d12d79f65be286965264c0705ce76b8fc3c6d93de331032b2b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812847"
---
# <a name="querying-for-available-properties"></a>Consultando propriedades disponíveis

Se você estiver escrevendo uma ferramenta de administração de uso geral, provavelmente precisará escrever rotinas para definir propriedades em generalidade total. Para dar suporte a isso, há um recurso que permite consultar dinamicamente as propriedades que estão disponíveis para os itens em qualquer coleção determinada.

A [**coleção PropertyInfo**](propertyinfo.md) está disponível em qualquer coleção que você possa estar mantendo. A **coleção PropertyInfo** contém um item para cada propriedade disponível. Você pode enumerar por meio desses itens para determinar se uma determinada propriedade está disponível.

Você pode obter a coleção [**PropertyInfo**](propertyinfo.md) de qualquer coleção que você está mantendo usando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) no [**objeto COMAdminCatalogCollection,**](comadmincatalogcollection.md) deixando o segundo parâmetro em branco em que normalmente especificaria a propriedade Key de um item pai.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Obter e definir propriedades](getting-and-setting-properties.md)
</dt> <dt>

[Interdependências entre propriedades](interdependencies-between-properties.md)
</dt> <dt>

[Salvando ou descartando alterações](saving-or-discarding-changes.md)
</dt> </dl>

 

 



