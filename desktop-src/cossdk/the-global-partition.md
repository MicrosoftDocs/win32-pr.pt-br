---
description: A partição global
ms.assetid: db11e6f5-0a3d-44ce-9a51-90d7e2b80981
title: A partição global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc218067bbf7170a1c2df6f306b6dfe5787ac2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457160"
---
# <a name="the-global-partition"></a>A partição global

Além de partições definidas pelo administrador e conjuntos de partição, há uma partição especial em cada computador chamada de *partição global*. Uma partição global é criada automaticamente quando o COM+ é instalado. A partição global foi projetada para conter aplicativos de todo o sistema que precisam ser acessíveis a todos os usuários em um servidor ou no domínio. A instalação de um aplicativo na partição global elimina a necessidade de instalar uma cópia do aplicativo em cada conjunto de partições do usuário individual.

Se o conjunto de partições de um usuário não incluir um aplicativo específico que o usuário está tentando acessar, mas esse aplicativo estiver instalado na partição global, o aplicativo será ativado da partição global. Nesse caso, no entanto, todos os componentes do aplicativo instalados na partição global devem ser marcados como componentes públicos, não privados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Partições padrão](default-partitions.md)
</dt> <dt>

[Partições locais](local-partitions.md)
</dt> <dt>

[Propriedades da partição](partition-properties.md)
</dt> <dt>

[Partições e Active Directory](partitions-and-active-directory.md)
</dt> </dl>

 

 



