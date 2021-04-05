---
description: Salvando ou descartando alterações
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Salvando ou descartando alterações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826254"
---
# <a name="saving-or-discarding-changes"></a>Salvando ou descartando alterações

Quando você define propriedades em um item, nenhuma alteração é realmente registrada no catálogo COM+ até que você salve explicitamente as alterações. Você faz isso usando o método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para a coleção que contém o item.

Se você quiser descartar as alterações que ainda não foram confirmadas, você pode chamar o método [**populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . Isso lê todos os dados persistentes do catálogo COM+ para todos os itens na coleção, excluindo efetivamente todas as alterações pendentes.

Quando você usa [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), todas as inconsistências nas configurações de propriedade escolhidas resultam em um erro e o **SaveChanges** não grava o objeto que retornou o erro. Todas as propriedades em um determinado item são gravadas ou não são gravadas como um todo.

No entanto, quando ocorrem erros de gravação, eles podem não ser devido a configurações incompatíveis; alguma outra falha pode ter ocorrido. Você precisa inspecionar os detalhes da falha para ter certeza. Para obter mais informações, consulte [lidando com erros de administração com+](handling-com--administration-errors.md) e [interdependências entre Propriedades](interdependencies-between-properties.md).

Como regra geral, quanto mais alterações você tentar salvar ao mesmo tempo, particularmente as alterações em vários objetos, mais provavelmente você receberá um erro e mais difícil será rastrear.

Além disso, entre as chamadas para [**popular**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), você não tem um bloqueio nos itens da coleção; a contenção é possível. Para obter mais detalhes, consulte [obtendo e Configurando Propriedades](getting-and-setting-properties.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Obtendo e definindo propriedades](getting-and-setting-properties.md)
</dt> <dt>

[Interdependências entre propriedades](interdependencies-between-properties.md)
</dt> <dt>

[Consultando as propriedades disponíveis](querying-for-available-properties.md)
</dt> </dl>

 

 



