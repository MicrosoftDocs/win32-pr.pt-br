---
title: Pipes assíncronos
description: O uso de parâmetros de pipe com RPC assíncrono permite transmitir dados de forma incremental, pois eles ficam disponíveis, sem ligar o cliente e o servidor.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641632"
---
# <a name="asynchronous-pipes"></a><span data-ttu-id="66771-103">Pipes assíncronos</span><span class="sxs-lookup"><span data-stu-id="66771-103">Asynchronous Pipes</span></span>

<span data-ttu-id="66771-104">O uso de parâmetros de [pipe](/windows/desktop/Midl/pipe) com RPC assíncrono permite transmitir dados de forma incremental, pois eles ficam disponíveis, sem ligar o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="66771-104">Using [pipe](/windows/desktop/Midl/pipe) parameters with asynchronous RPC allows you to transmit data incrementally, as it becomes available, without tying up the client and server.</span></span> <span data-ttu-id="66771-105">Isso é particularmente útil quando você tem uma grande quantidade de dados a serem transferidos, combinados com um cliente lento, um servidor lento ou uma rede lenta.</span><span class="sxs-lookup"><span data-stu-id="66771-105">This is particularly useful when you have a large amount of data to transfer, combined with a slow client, a slow server, or a slow network.</span></span> <span data-ttu-id="66771-106">Se você usar um pipe em uma chamada de função assíncrona, ele será, por definição, um pipe assíncrono.</span><span class="sxs-lookup"><span data-stu-id="66771-106">If you use a pipe in an asynchronous function call, it is, by definition, an asynchronous pipe.</span></span> <span data-ttu-id="66771-107">Não há suporte para pipes síncronos em conjunto com funções assíncronas.</span><span class="sxs-lookup"><span data-stu-id="66771-107">Synchronous pipes are not supported in conjunction with asynchronous functions.</span></span>

<span data-ttu-id="66771-108">Ao contrário dos pipes convencionais (síncronos) em que o servidor lida com todos os detalhes de envio e recebimento de dados de pipe, os pipes assíncronos são simétricos.</span><span class="sxs-lookup"><span data-stu-id="66771-108">Unlike conventional (synchronous) pipes where the server handles all the details of sending and receiving pipe data, asynchronous pipes are symmetrical.</span></span> <span data-ttu-id="66771-109">Ou seja, o cliente e o servidor podem enviar e extrair dados por meio do pipe.</span><span class="sxs-lookup"><span data-stu-id="66771-109">That is, both the client and the server can push and pull data through the pipe.</span></span>

> [!Note]  
> <span data-ttu-id="66771-110">Os parâmetros de pipe só podem ser passados por referência.</span><span class="sxs-lookup"><span data-stu-id="66771-110">Pipe parameters can only be passed by reference.</span></span> <span data-ttu-id="66771-111">Mesmo que o arquivo IDL mostre os parâmetros de [pipe](/windows/desktop/Midl/pipe) que estão sendo passados pelo valor, os stubs gerados aceitarão os parâmetros de pipe por referência apenas.</span><span class="sxs-lookup"><span data-stu-id="66771-111">Even if the IDL file shows [pipe](/windows/desktop/Midl/pipe) parameters being passed by value, the generated stubs will accept pipe parameters by reference only.</span></span>

 

<span data-ttu-id="66771-112">Na seguinte discussão sobre pipes assíncronos, a familiaridade com o construtor de tipo de pipe é assumida.</span><span class="sxs-lookup"><span data-stu-id="66771-112">In the following discussion of asynchronous pipes, familiarity with the pipe type constructor is assumed.</span></span> <span data-ttu-id="66771-113">Para obter mais informações sobre os procedimentos de pipe descritos nestes tópicos, consulte [pipes](pipes.md).</span><span class="sxs-lookup"><span data-stu-id="66771-113">For more information on the pipe procedures described in these topics, see [Pipes](pipes.md).</span></span>

 

 