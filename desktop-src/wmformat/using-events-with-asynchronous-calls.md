---
title: Usando eventos com chamadas assíncronas
description: Usando eventos com chamadas assíncronas
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- SDK do Windows Media Format, eventos com chamadas assíncronas
- SDK do Windows Media Format, eventos de chamada assíncrona
- eventos, chamadas assíncronas
- eventos de chamada assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364326"
---
# <a name="using-events-with-asynchronous-calls"></a><span data-ttu-id="ea5a9-107">Usando eventos com chamadas assíncronas</span><span class="sxs-lookup"><span data-stu-id="ea5a9-107">Using Events with Asynchronous Calls</span></span>

<span data-ttu-id="ea5a9-108">Frequentemente, ao usar métodos que são chamados de forma assíncrona, você desejará interromper o processamento adicional de seu aplicativo até que o método conclua o processamento.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-108">Frequently, when using methods that are called asynchronously, you will want to halt further processing of your application until after the method completes processing.</span></span> <span data-ttu-id="ea5a9-109">Você pode implementar qualquer técnica que desejar para lidar com essa situação.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-109">You can implement any technique you like to handle this situation.</span></span> <span data-ttu-id="ea5a9-110">Esta seção descreve como usar um evento para aguardar chamadas assíncronas no thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-110">This section describes using an event to wait for asynchronous calls in the calling thread.</span></span> <span data-ttu-id="ea5a9-111">Essa técnica é frequentemente usada com o Windows Media Format SDK e é demonstrada em alguns dos aplicativos de exemplo.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-111">This technique is frequently used with the Windows Media Format SDK, and is demonstrated in some of the sample applications.</span></span>

<span data-ttu-id="ea5a9-112">A lista a seguir resume o uso de eventos para aguardar chamadas assíncronas.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-112">The following list summarizes the use of events to wait for asynchronous calls.</span></span>

1.  <span data-ttu-id="ea5a9-113">Crie um evento para usar com seu aplicativo chamando a função **CreateEvent** do SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-113">Create an event for use with your application by calling the **CreateEvent** function of the Platform SDK.</span></span>
2.  <span data-ttu-id="ea5a9-114">Ao implementar os retornos de chamada apropriados para seu aplicativo, intercepte as mensagens para as quais você precisa aguardar.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-114">When implementing the appropriate callbacks for your application, trap the messages for which you need to wait.</span></span> <span data-ttu-id="ea5a9-115">Na lógica de tratamento de mensagens para as mensagens desejadas, sinalize o evento chamando a função **SetEvent** do SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-115">In the message handling logic for the desired messages, signal the event by calling the **SetEvent** function of the Platform SDK.</span></span>
3.  <span data-ttu-id="ea5a9-116">Depois que as chamadas para eventos assíncronos são feitas em seu aplicativo, aguarde o evento ser sinalizado chamando a função **WaitForSingleObject** do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-116">After calls to asynchronous events are made in your application, wait for the event to signal by calling the **WaitForSingleObject** function of the Platform SDK.</span></span> <span data-ttu-id="ea5a9-117">Se você estiver criando um aplicativo do Windows, deverá criar um loop para verificar se há mensagens do Windows e incluir uma chamada para **WaitForSingleObject** no loop com um tempo de espera curto.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-117">If you are designing a Windows application, you should create a loop to check for Windows messages and include a call to **WaitForSingleObject** in the loop with a short wait time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea5a9-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea5a9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea5a9-119">**Usando os métodos de retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="ea5a9-119">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




