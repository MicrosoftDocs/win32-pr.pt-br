---
description: Registrando e ativando componentes em partições
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Registrando e ativando componentes em partições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500920"
---
# <a name="registering-and-activating-components-in-partitions"></a>Registrando e ativando componentes em partições

Depois que uma partição tiver sido criada, a próxima etapa será registrar os componentes COM+ dentro dessa partição. Um componente é registrado em uma partição quando um novo aplicativo COM+ é criado ou quando um aplicativo COM+ existente é instalado na partição. Para facilitar a administração do registro quando várias partições contêm os mesmos componentes COM+, o serviço de partições permite que um administrador Copie aplicativos ou componentes de uma partição para outra. Quando um aplicativo COM+ ou um componente é copiado, todas as propriedades de partição associadas são copiadas com ele, exceto a identidade do aplicativo ou qualquer um dos membros de uma função.

Quando o programa cliente chama a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) para criar uma instância de um objeto, o com+ executa duas etapas distintas, da seguinte maneira:

1.  Localiza a partição na qual o componente reside
2.  Localiza o componente correto dentro dessa partição

Os tópicos a seguir nesta seção descrevem essas etapas em detalhes:

-   [Localizando partições durante a ativação](locating-partitions-during-activation.md)
-   [Localizando um componente para ativação](locating-a-component-for-activation.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Restrições de design de aplicativo](application-design-restrictions.md)
</dt> <dt>

[Componentes e partições em fila COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementação de partição](partition-implementation.md)
</dt> <dt>

[O que são partições COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 
