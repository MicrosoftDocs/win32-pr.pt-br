---
title: Erro
description: Erro
ms.assetid: d3a087e4-7b57-4070-aa82-3673bc18a54f
keywords:
- Funções de retorno de chamada do AVICap, mensagens de notificação de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f418f16ae2af15902e96927990d79a4ecac08b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005937"
---
# <a name="error"></a><span data-ttu-id="06b08-104">Erro</span><span class="sxs-lookup"><span data-stu-id="06b08-104">Error</span></span>

<span data-ttu-id="06b08-105">Uma janela de captura usa mensagens de notificação de erro para notificar o aplicativo sobre erros AVICap, como ficar sem espaço em disco, tentar gravar em um arquivo somente leitura, falha ao acessar o hardware ou descartar muitos quadros.</span><span class="sxs-lookup"><span data-stu-id="06b08-105">A capture window uses error notification messages to notify your application of AVICap errors, such as running out of disk space, attempting to write to a read-only file, failing to access hardware, or dropping too many frames.</span></span> <span data-ttu-id="06b08-106">O conteúdo de uma notificação de erro inclui um identificador de mensagem e uma cadeia de texto formatada pronta para exibição.</span><span class="sxs-lookup"><span data-stu-id="06b08-106">The content of an error notification includes a message identifier and a formatted text string ready for display.</span></span> <span data-ttu-id="06b08-107">Seu aplicativo pode usar o identificador de mensagem para filtrar as notificações e limitar as mensagens a apresentar ao usuário.</span><span class="sxs-lookup"><span data-stu-id="06b08-107">Your application can use the message identifier to filter the notifications and limit the messages to present to the user.</span></span> <span data-ttu-id="06b08-108">Um identificador de mensagem igual a zero indica que uma nova operação está sendo iniciada e a função de retorno de chamada deve limpar qualquer mensagem de erro exibida.</span><span class="sxs-lookup"><span data-stu-id="06b08-108">A message identifier of zero indicates a new operation is starting and the callback function should clear any displayed error message.</span></span>

 

 




