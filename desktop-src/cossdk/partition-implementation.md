---
description: Quando instalado em um servidor de aplicativos, o COM+ cria automaticamente uma partição, conhecida como partição global.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Implementação de partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3014aac80e853ca387538faf034eeadae91dd70cf36931de34638cbcbec7b02f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047344"
---
# <a name="partition-implementation"></a>Implementação de partição

Quando instalado em um servidor de aplicativos, o COM+ cria automaticamente uma partição, conhecida como a *partição global*. A partição global inclui um conjunto padrão de aplicativos COM+. Os aplicativos COM+ instalados na partição global estão disponíveis automaticamente para todos os usuários no servidor. Se você tiver outros aplicativos COM+ que gostaria de disponibilizar para todos os usuários no servidor, poderá adicioná-los à partição global.

Além da partição global, você pode criar outras partições somente para usuários nesse servidor ou para usuários em todo o domínio. Criar partições adicionais e instalar várias configurações de um aplicativo COM+ neles permite que os usuários executem essas configurações de aplicativo simultaneamente no mesmo computador. Além disso, ao instalar aplicativos COM+ em uma partição diferente da partição global, você pode controlar o acesso do usuário a esses aplicativos.

**Windows XP:** A capacidade de criar, configurar ou delegar partições COM+ não está disponível. A partição global é a única partição COM+ disponível.

Para obter mais informações sobre partições e partições locais definidas no Active Directory, consulte os seguintes tópicos:

-   [Partições locais](local-partitions.md)
-   [Partições e Active Directory](partitions-and-active-directory.md)
-   [Partições padrão](default-partitions.md)
-   [A partição global](the-global-partition.md)
-   [Propriedades da partição](partition-properties.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Restrições de design do aplicativo](application-design-restrictions.md)
</dt> <dt>

[Partições e componentes em fila COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Registrando e ativando componentes em partições](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[O que são partições COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



