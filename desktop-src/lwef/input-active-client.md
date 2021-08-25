---
title: Input-Active cliente
description: Input-Active cliente
ms.assetid: b46e91d3-eca7-4a4a-b1ce-27b5e6ad92a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9555b614a30e73df0cc7d1d81cd8192480d49261a32e8be8d164bdb277e4c0f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943956"
---
# <a name="input-active-client"></a>Input-Active cliente

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Como vários aplicativos cliente podem compartilhar o mesmo caractere e como vários clientes podem usar  caracteres diferentes ao mesmo tempo, o servidor designa um cliente como o cliente ativo de entrada e envia o mouse e a entrada de voz somente para esse aplicativo cliente. Isso mantém o gerenciamento de ordem da entrada do usuário, para que um cliente apropriado responda à entrada.

Normalmente, a interação do usuário determina qual aplicativo cliente se torna ativo de entrada. Por exemplo, se o usuário clicar em um caractere, o aplicativo cliente desse caractere se tornará input-active. Da mesma forma, se um usuário falar o nome de um caractere, ele se tornará input-active. Além disso, quando o servidor processa o método [**Show**](show-method.md) de um caractere, o cliente desse caractere se torna input-active.

Quando um caractere estiver oculto, o cliente desse caractere não será mais ativo de entrada para esse caractere. O servidor torna automaticamente o cliente ativo de quaisquer caracteres restantes de entrada ativos. Quando todos os caracteres estão ocultos, nenhum cliente está ativo de entrada. No entanto, nessa situação, se o usuário pressionar a tecla de acesso Escutando, o Agent continuará a escutar seus comandos (usando o mecanismo de reconhecimento de fala que corresponde ao caractere mais alto do último cliente ativo de entrada).

Se vários clientes compartilharem o mesmo caractere, o servidor designará seu *cliente ativo* como cliente ativo de entrada. O caractere ativo é o mais alto na ordem do cliente. Você pode definir seu cliente como o cliente ativo ou não ativo usando o [**método Activate.**](activate-method.md) Você também pode usar o **método Activate** para tornar explicitamente a entrada do cliente ativa; mas para evitar interromper outros clientes do caractere, você deve fazer isso somente quando o aplicativo cliente estiver ativo. Por exemplo, se o usuário clicar na janela do aplicativo, ativando seu aplicativo, você poderá chamar o método **Activate** para receber e processar a entrada do mouse e da fala direcionada para o caractere.

 

 




