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
# <a name="receiving-a-response"></a><span data-ttu-id="53d0e-103">Recebendo uma resposta</span><span class="sxs-lookup"><span data-stu-id="53d0e-103">Receiving a Response</span></span>

<span data-ttu-id="53d0e-104">Como os componentes enfileirados são projetados para funcionar de forma assíncrona, os aplicativos cliente não devem bloquear enquanto aguardam uma resposta de uma solicitação em fila.</span><span class="sxs-lookup"><span data-stu-id="53d0e-104">Because queued components are designed to work asynchronously, client applications should not block while waiting for a response from a queued request.</span></span> <span data-ttu-id="53d0e-105">No entanto, geralmente é útil para o aplicativo cliente ou um aplicativo relacionado no computador cliente receber uma resposta eventualmente.</span><span class="sxs-lookup"><span data-stu-id="53d0e-105">Nevertheless, it is often useful for the client application or a related application on the client machine to receive a response eventually.</span></span> <span data-ttu-id="53d0e-106">Por exemplo, um cliente pode querer ser notificado quando uma transação solicitada tiver sido concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="53d0e-106">For example, a client may want to be notified when a requested transaction has been completed successfully.</span></span>

<span data-ttu-id="53d0e-107">Há várias maneiras para um componente em fila enviar uma resposta de volta para seu chamador de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="53d0e-107">There are a variety of ways for a queued component to send a response back to its caller asynchronously.</span></span> <span data-ttu-id="53d0e-108">Por exemplo, ele pode enviar um email.</span><span class="sxs-lookup"><span data-stu-id="53d0e-108">For example, it could send an email.</span></span> <span data-ttu-id="53d0e-109">Como alternativa, o servidor pode publicar eventos livremente acoplados aos quais o cliente poderia assinar.</span><span class="sxs-lookup"><span data-stu-id="53d0e-109">Alternatively, the server could publish loosely coupled events to which the client could subscribe.</span></span>

<span data-ttu-id="53d0e-110">Outra maneira de um cliente obter uma resposta de um componente em fila que é executado em um servidor é o cliente passar o método chamado um objeto de notificação.</span><span class="sxs-lookup"><span data-stu-id="53d0e-110">Another way for a client to obtain a response from a queued component that runs on a server is for the client to pass the called method a notification object.</span></span> <span data-ttu-id="53d0e-111">Um objeto de notificação é uma instância de um componente em fila que é executado no cliente.</span><span class="sxs-lookup"><span data-stu-id="53d0e-111">A notification object is an instance of a queued component that runs on the client.</span></span> <span data-ttu-id="53d0e-112">Esse objeto de notificação pode ser bastante simples, contendo apenas um inteiro que é usado para representar um valor de erro ou pode ser bastante complexo, contendo todas as informações necessárias para reverter uma transação no cliente.</span><span class="sxs-lookup"><span data-stu-id="53d0e-112">Such a notification object might be quite simple, containing only an integer that is used to represent an error value, or it might be quite complex, containing all the information necessary to roll back a transaction on the client.</span></span> <span data-ttu-id="53d0e-113">Em ambos os casos, o cliente de chamada passa um objeto de notificação como um parâmetro de entrada sempre que ele desejar uma resposta de um componente em fila que é executado em um servidor.</span><span class="sxs-lookup"><span data-stu-id="53d0e-113">In either case, the calling client passes a notification object as an input parameter whenever it desires a response from a queued component that runs on a server.</span></span> <span data-ttu-id="53d0e-114">Como o objeto de notificação é enfileirado, o servidor pode chamar seus métodos para alterar seu estado, o que pode ser posteriormente lido pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="53d0e-114">Because the notification object is queued, the server can call on its methods to alter its state, which can subsequently be read out by the client.</span></span> <span data-ttu-id="53d0e-115">Nesse cenário, o serviço de componentes em fila COM+ é usado no cliente e no servidor para permitir a comunicação assíncrona em ambas as direções.</span><span class="sxs-lookup"><span data-stu-id="53d0e-115">In this scenario, the COM+ queued components service is used on both the client and the server to allow asynchronous communication in both directions.</span></span>

 

 



