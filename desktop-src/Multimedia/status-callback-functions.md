---
title: Funções de retorno de chamada de status
description: Funções de retorno de chamada de status
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Funções de retorno de chamada AVICap, status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b4b4bf4cad5f689f1e146986f9d1b55b00f1aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364000"
---
# <a name="status-callback-functions"></a><span data-ttu-id="8a08e-104">Funções de retorno de chamada de status</span><span class="sxs-lookup"><span data-stu-id="8a08e-104">Status Callback Functions</span></span>

<span data-ttu-id="8a08e-105">Uma janela de captura pode enviar mensagens para a função de retorno de chamada de status durante a captura de vídeo em disco ou durante outras operações demoradas para notificar seu aplicativo sobre o progresso de uma operação.</span><span class="sxs-lookup"><span data-stu-id="8a08e-105">A capture window can send messages to the status callback function while capturing video to disk or during other lengthy operations to notify your application of the progress of an operation.</span></span> <span data-ttu-id="8a08e-106">As informações de status incluem um identificador de mensagem e uma cadeia de texto formatada pronta para exibição.</span><span class="sxs-lookup"><span data-stu-id="8a08e-106">The status information includes a message identifier and a formatted text string ready for display.</span></span> <span data-ttu-id="8a08e-107">Seu aplicativo pode usar o identificador de mensagem para filtrar as notificações e limitar as mensagens a apresentar ao usuário.</span><span class="sxs-lookup"><span data-stu-id="8a08e-107">Your application can use the message identifier to filter the notifications and limit the messages to present to the user.</span></span> <span data-ttu-id="8a08e-108">Durante as operações de captura, a primeira mensagem enviada para a função de retorno de chamada é sempre IDS \_ \_ de início e a última é sempre IDs \_ \_ end.</span><span class="sxs-lookup"><span data-stu-id="8a08e-108">During capture operations, the first message sent to the callback function is always IDS\_CAP\_BEGIN and the last is always IDS\_CAP\_END.</span></span> <span data-ttu-id="8a08e-109">Um identificador de mensagem igual a zero indica que uma nova operação está sendo iniciada e a função de retorno de chamada deve limpar o status atual.</span><span class="sxs-lookup"><span data-stu-id="8a08e-109">A message identifier of zero indicates a new operation is starting and the callback function should clear the current status.</span></span>

 

 




