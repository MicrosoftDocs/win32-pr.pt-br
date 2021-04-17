---
description: Você pode modelar um provedor de classe como um provedor de Push ou pull, que especifica como um provedor espera interagir com o WMI.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Determinando o status de Push ou pull
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee037b4c81e43080ee119540b05568eb00cdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812080"
---
# <a name="determining-push-or-pull-status"></a>Determinando o status de Push ou pull

Você pode modelar um provedor de classe como um provedor de Push ou pull, que especifica como um provedor espera interagir com o WMI. Os provedores de pull recebem uma solicitação do WMI e atendem à solicitação gerando os dados dinamicamente ou recuperando-os de um cache local. Os provedores de pull também devem implementar um grande número de interfaces.

Um provedor de pull gera definições de classe dinamicamente. Normalmente, os dados gerenciados por um provedor de pull são alterados com frequência, exigindo que o provedor gere a classe dinamicamente ou recupere a classe de um cache local sempre que um aplicativo emitir uma solicitação. Um provedor de pull deve implementar seus próprios mecanismos de recuperação de dados, cache e notificação de eventos. Como a maioria dos provedores são provedores de pull, a documentação neste arquivo pressupõe que você está criando um provedor de pull, a menos que explicitamente declarado de outra forma.

Por outro lado, o WMI usa dados no repositório do WMI para lidar com todas as solicitações de aplicativos para provedores de envio por push. Os provedores de push também usam menos métodos de interface e, portanto, são mais fáceis de implementar. Um provedor de push usa o repositório WMI como uma área de armazenamento para obter informações sobre o objeto gerenciado e atualiza essas informações somente durante a inicialização. Por exemplo, o provedor de classes WDM incluído na seção WMI do SDK (Software Development Kit) do Microsoft Windows é modelado como um provedor de push.

Usando o repositório WMI como uma área de armazenamento, um provedor de push Obtém os seguintes benefícios em um provedor de pull:

-   O provedor não precisa implementar um cache local para armazenar dados.
-   O provedor não precisa dar suporte à recuperação de dados; em vez disso, o provedor pode contar com o WMI para fornecer suporte de recuperação.
-   Quando um aplicativo solicita dados fornecidos pelo provedor, o WMI atende a essa solicitação.
-   O provedor também pode contar com o WMI para dar suporte à notificação de eventos.

No entanto, como um provedor Push é atualizado somente durante a inicialização, qualquer alteração em uma classe pode não ser refletida no repositório WMI por algum tempo. Portanto, o modelo de provedor Push funciona melhor com classes que mudam pouco ou são completamente estáticas.

 

 



