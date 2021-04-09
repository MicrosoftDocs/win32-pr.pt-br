---
description: Consultando as propriedades disponíveis
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Consultando as propriedades disponíveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089497"
---
# <a name="querying-for-available-properties"></a>Consultando as propriedades disponíveis

Se você estiver escrevendo uma ferramenta de administração de finalidade geral, provavelmente precisará escrever rotinas para definir propriedades de forma completa. Para dar suporte a isso, há uma instalação que permite que você consulte dinamicamente as propriedades que estão disponíveis para os itens em qualquer coleção específica.

A coleção [**PropertyInfo**](propertyinfo.md) está disponível em qualquer coleção que você esteja mantendo. A coleção **PropertyInfo** contém um item para cada propriedade disponível. Você pode enumerar esses itens para determinar se uma determinada propriedade está disponível.

Você pode obter a coleção [**PropertyInfo**](propertyinfo.md) de qualquer coleção que você esteja mantendo usando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , deixando o segundo parâmetro em branco, em que você normalmente especificaria a propriedade de chave de um item pai.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Obtendo e definindo propriedades](getting-and-setting-properties.md)
</dt> <dt>

[Interdependências entre propriedades](interdependencies-between-properties.md)
</dt> <dt>

[Salvando ou descartando alterações](saving-or-discarding-changes.md)
</dt> </dl>

 

 



