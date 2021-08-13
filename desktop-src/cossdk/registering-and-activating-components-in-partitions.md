---
description: Registrando e ativando componentes em partições
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Registrando e ativando componentes em partições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf17787c953e3fe615432a8100fa71390e8aa3b8c90453a310813207ba5df7fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547058"
---
# <a name="registering-and-activating-components-in-partitions"></a>Registrando e ativando componentes em partições

Depois que uma partição tiver sido criada, a próxima etapa será registrar seus componentes COM+ dentro dessa partição. Um componente é registrado em uma partição quando um novo aplicativo COM+ é criado ou quando um aplicativo COM+ existente é instalado na partição. Para facilitar a administração do registro quando várias partições contêm os mesmos componentes COM+, o serviço de partições permite que um administrador copie aplicativos ou componentes de uma partição para outra. Quando um aplicativo COM+ ou um componente é copiado, todas as propriedades de partição associadas são copiadas com ele, exceto a identidade do aplicativo ou qualquer um dos membros de uma função.

Quando o programa cliente chama a [**função CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) para insinciar um objeto, o COM+ executa duas etapas distintas, da seguinte forma:

1.  Localiza a partição na qual o componente reside
2.  Localiza o componente correto dentro dessa partição

Os tópicos a seguir nesta seção descrevem estas etapas em detalhes:

-   [Localizando partições durante a ativação](locating-partitions-during-activation.md)
-   [Localizando um componente para ativação](locating-a-component-for-activation.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Restrições de design do aplicativo](application-design-restrictions.md)
</dt> <dt>

[Partições e componentes em fila COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementação de partição](partition-implementation.md)
</dt> <dt>

[O que são partições COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 
