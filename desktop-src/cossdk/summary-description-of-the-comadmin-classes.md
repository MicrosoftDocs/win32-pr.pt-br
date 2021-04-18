---
description: Há três classes fornecidas pela biblioteca COMAdmin (comadmin.dll), cada uma implementando uma interface COM dupla.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Descrição resumida das classes COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753204"
---
# <a name="summary-description-of-the-comadmin-classes"></a>Descrição resumida das classes COMAdmin

Há três classes fornecidas pela biblioteca COMAdmin (comadmin.dll), cada uma implementando uma interface COM dupla. Você usa objetos criados a partir dessas classes para obter acesso ao catálogo, para representar as coleções no catálogo e para representar os itens contidos nas coleções.

## <a name="comadmincatalog"></a>COMAdminCatalog

A classe [**COMAdminCatalog**](comadmincatalog.md) representa o próprio catálogo. Um objeto criado a partir de **COMAdminCatalog** é o objeto fundamental que você usa na administração programática. Além de estabelecer a conexão básica com o servidor de catálogo ao instanciá-lo, o **COMAdminCatalog** fornece métodos que permitem que você faça o seguinte:

-   Obter coleções no catálogo.
-   Conecte-se ao servidor de catálogo em um computador remoto.
-   Instale, exporte, inicie, desligue e obtenha informações sobre aplicativos COM+.
-   Instale componentes em aplicativos COM+ e obtenha informações sobre componentes.
-   Iniciar, parar ou atualizar serviços em execução no computador.
-   Atualizar, restaurar ou fazer backup de informações do catálogo.

No COM+ 1,0, a classe [**COMAdminCatalog**](comadmincatalog.md) implementa a interface [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) . No COM+ 1,5, a classe **COMAdminCatalog** implementa [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) como sua interface padrão.

## <a name="comadmincatalogcollection"></a>COMAdminCatalogCollection

A classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) representa qualquer coleção no catálogo, fornecendo uma cadeia de caracteres que nomeia a coleção específica no tempo de instanciação do objeto. (As coleções de catálogos disponíveis são nomeadas na tabela em [coleções de administração com+](com--administration-collections.md).) Os objetos são criados dessa classe ao recuperar uma coleção de nível superior chamando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) do objeto [**COMAdminCatalog**](comadmincatalog.md) . Esses objetos também são criados ao recuperar uma coleção filho chamando o método **GetCollection** de seu objeto de coleção pai. Os objetos **COMAdminCatalogCollection** permitem que você faça o seguinte:

-   Enumere os itens contidos na coleção.
-   Recuperar um item da coleção.
-   Adicionar ou remover itens da coleção.
-   Salve ou descarte as alterações pendentes feitas na coleção ou nos itens que ela contém.
-   Obtenha uma coleção diferente no catálogo.

A classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa a interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) .

## <a name="comadmincatalogobject"></a>COMAdminCatalogObject

A classe [**COMAdminCatalogObject**](comadmincatalogobject.md) representa qualquer item contido em uma coleção. Os objetos são criados dessa classe ao obter um item por meio da propriedade [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) de um objeto de coleção de catálogo. Os objetos criados a partir da classe **COMAdminCatalogObject** permitem que você faça o seguinte:

-   As propriedades Get ou set com suporte no item que o objeto está sendo usado para representar.
-   Obtenha informações sobre o item e suas propriedades.

A classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa a interface [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando o catálogo COM+](accessing-the-com--catalog.md)
</dt> <dt>

[Visão geral dos objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 



