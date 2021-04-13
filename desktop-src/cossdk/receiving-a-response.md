---
description: Recebendo uma resposta
ms.assetid: 48919608-a102-43e2-9ca0-80b17344b5eb
title: Recebendo uma resposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9e05ec392b7db828ad1efd1360c4d4fb232210
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501082"
---
# <a name="receiving-a-response"></a>Recebendo uma resposta

Como os componentes enfileirados são projetados para funcionar de forma assíncrona, os aplicativos cliente não devem bloquear enquanto aguardam uma resposta de uma solicitação em fila. No entanto, geralmente é útil para o aplicativo cliente ou um aplicativo relacionado no computador cliente receber uma resposta eventualmente. Por exemplo, um cliente pode querer ser notificado quando uma transação solicitada tiver sido concluída com êxito.

Há várias maneiras para um componente em fila enviar uma resposta de volta para seu chamador de forma assíncrona. Por exemplo, ele pode enviar um email. Como alternativa, o servidor pode publicar eventos livremente acoplados aos quais o cliente poderia assinar.

Outra maneira de um cliente obter uma resposta de um componente em fila que é executado em um servidor é o cliente passar o método chamado um objeto de notificação. Um objeto de notificação é uma instância de um componente em fila que é executado no cliente. Esse objeto de notificação pode ser bastante simples, contendo apenas um inteiro que é usado para representar um valor de erro ou pode ser bastante complexo, contendo todas as informações necessárias para reverter uma transação no cliente. Em ambos os casos, o cliente de chamada passa um objeto de notificação como um parâmetro de entrada sempre que ele desejar uma resposta de um componente em fila que é executado em um servidor. Como o objeto de notificação é enfileirado, o servidor pode chamar seus métodos para alterar seu estado, o que pode ser posteriormente lido pelo cliente. Nesse cenário, o serviço de componentes em fila COM+ é usado no cliente e no servidor para permitir a comunicação assíncrona em ambas as direções.

 

 



