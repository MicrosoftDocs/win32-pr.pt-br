---
title: O estado do pipe
description: No servidor, o compilador MIDL cria uma variável de estado que coordena os procedimentos de push, pull e Alloc.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084696"
---
# <a name="the-pipe-state"></a><span data-ttu-id="87bd9-103">O estado do pipe</span><span class="sxs-lookup"><span data-stu-id="87bd9-103">The Pipe State</span></span>

<span data-ttu-id="87bd9-104">No servidor, o compilador MIDL cria uma variável de *estado* que coordena os procedimentos de push, pull e Alloc.</span><span class="sxs-lookup"><span data-stu-id="87bd9-104">On the server, the MIDL compiler creates a *state* variable that coordinates push, pull, and alloc procedures.</span></span> <span data-ttu-id="87bd9-105">No lado do cliente, o desenvolvedor deve criar a variável de *estado* .</span><span class="sxs-lookup"><span data-stu-id="87bd9-105">On the client side, the developer must create the *state* variable.</span></span> <span data-ttu-id="87bd9-106">Portanto, a variável de *estado* é local para ambos os lados — ou seja, o cliente e o servidor mantêm seu próprio estado de pipe.</span><span class="sxs-lookup"><span data-stu-id="87bd9-106">Therefore, the *state* variable is local to both sides—that is, the client and server each maintain their own pipe state.</span></span> <span data-ttu-id="87bd9-107">O código stub do servidor mantém a variável de estado no servidor.</span><span class="sxs-lookup"><span data-stu-id="87bd9-107">The server stub code maintains the state variable on the server.</span></span> <span data-ttu-id="87bd9-108">Você não deve tentar modificar seu conteúdo diretamente.</span><span class="sxs-lookup"><span data-stu-id="87bd9-108">You should not attempt to modify its contents directly.</span></span> <span data-ttu-id="87bd9-109">O cliente deve inicializar os campos na estrutura de controle de pipe e manter sua variável de *estado* .</span><span class="sxs-lookup"><span data-stu-id="87bd9-109">The client must initialize the fields in the pipe control structure and maintain its *state* variable.</span></span> <span data-ttu-id="87bd9-110">Ele usa a variável de *estado* para identificar onde localizar ou colocar dados.</span><span class="sxs-lookup"><span data-stu-id="87bd9-110">It uses the *state* variable to identify where to locate or place data.</span></span>

<span data-ttu-id="87bd9-111">A variável de *estado* do cliente pode ser tão simples quanto um identificador de arquivo, se você estiver transferindo dados de um arquivo para outro.</span><span class="sxs-lookup"><span data-stu-id="87bd9-111">The client *state* variable can be as simple as a file handle, if you are transferring data from one file to another.</span></span> <span data-ttu-id="87bd9-112">Ele também pode ser um inteiro que aponta para um elemento em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="87bd9-112">It can also be an integer that points to an element in an array.</span></span> <span data-ttu-id="87bd9-113">Ou você pode definir uma estrutura de estado bastante complexa para executar tarefas adicionais, como coordenar as rotinas de push e pull em um \[ parâmetro [in](/windows/desktop/Midl/in)e [out](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="87bd9-113">Or you can define a fairly complex state structure to perform additional tasks, such as coordinating the push and pull routines on an \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl)\] parameter.</span></span>

 

 