---
title: Input-Active cliente
description: Input-Active cliente
ms.assetid: b46e91d3-eca7-4a4a-b1ce-27b5e6ad92a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3223ddc7bb412b333d628f93cc56b27efd0abb7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292502"
---
# <a name="input-active-client"></a>Input-Active cliente

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Como vários aplicativos cliente podem compartilhar o mesmo caractere e, como vários clientes podem usar caracteres diferentes ao mesmo tempo, o servidor designa um cliente como o cliente de *entrada-ativo* e envia a entrada de mouse e voz somente para esse aplicativo cliente. Isso mantém o gerenciamento ordenado da entrada do usuário, para que um cliente apropriado responda à entrada.

Normalmente, a interação do usuário determina qual aplicativo cliente torna-se ativo. Por exemplo, se o usuário clicar em um caractere, o aplicativo cliente desse caractere se tornará entrada-ativo. Da mesma forma, se um usuário falasse o nome de um caractere, ele se tornará entrada-ativo. Além disso, quando o servidor processa o método [**show**](show-method.md) de um caractere, o cliente desse caractere torna-se ativo.

Quando um caractere estiver oculto, o cliente desse caractere não estará mais ativo para esse caractere. O servidor torna automaticamente o cliente ativo de qualquer caractere restante (s) entrada-ativo. Quando todos os caracteres estão ocultos, nenhum cliente é inserido-ativo. No entanto, nessa situação, se o usuário pressionar a tecla de atalho de escuta, o Agent continuará a escutar seus comandos (usando o mecanismo de reconhecimento de fala que corresponde ao caractere superior do último cliente de entrada-ativo).

Se vários clientes estiverem compartilhando o mesmo caractere, o servidor designará seu *cliente ativo* como entrada-cliente ativo. O caractere ativo é o primeiro na ordem do cliente. Você pode definir seu cliente para ser o cliente ativo ou não ativo usando o método [**Ativar**](activate-method.md) . Você também pode usar o método **Activate** para tornar explicitamente a entrada do cliente-ativa; Mas, para evitar a interrupção de outros clientes do caractere, você deve fazer isso somente quando o aplicativo cliente estiver ativo. Por exemplo, se o usuário clicar na janela do aplicativo, ativando seu aplicativo, você poderá chamar o método **Activate** para receber e processar a entrada de mouse e fala direcionada para o caractere.

 

 




