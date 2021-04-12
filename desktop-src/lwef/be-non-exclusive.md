---
title: Ser não exclusivo
description: Ser não exclusivo
ms.assetid: 7a44840d-6bf9-4c12-ba14-66d7067a984d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b637bcf0860ccc4917b1af344664f9828b0da8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363830"
---
# <a name="be-non-exclusive"></a>Ser não exclusivo

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Os caracteres interativos podem ser empregados na interface do usuário como assistentes, guias, entretenimentos, histórias, agentes de vendas ou em uma variedade de outras funções. Um caractere que executa ou ajuda automaticamente não deve ser projetado ao contrário do princípio de design para manter o usuário no controle. Ao adicionar um caractere à interface de um site ou aplicativo convencional, use o caractere como um aprimoramento, em vez de uma substituição de, a interface primária. Evite implementar qualquer recurso ou operação que exija exclusivamente um caractere.

Da mesma forma, permita que o usuário escolha quando deseja interagir com seu caractere. Um usuário deve ser capaz de ignorar o caractere e retorná-lo somente com a permissão do usuário. Forçar a interação de caracteres em usuários pode ter um sério efeito negativo. Para dar suporte ao controle de usuário da interação de caracteres, o Microsoft Agent inclui automaticamente os comandos ocultar e mostrar. A API do Microsoft Agent também dá suporte a esses métodos, de modo que você pode incluir suporte para essas funções em sua própria interface. Além disso, a interface do usuário do Microsoft Agent inclui propriedades globais que permitem ao usuário substituir determinadas opções de saída de caracteres. Para garantir que as preferências do usuário sejam mantidas, essas propriedades não podem ser substituídas por meio da API.

 

 




