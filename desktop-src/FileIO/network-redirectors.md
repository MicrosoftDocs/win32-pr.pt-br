---
description: Descreve a funcionalidade de um redirecionador de rede.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Redirecionadores de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce8c887cba779fe3f6aee9811819c6638d926f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837337"
---
# <a name="network-redirectors"></a><span data-ttu-id="5521b-103">Redirecionadores de rede</span><span class="sxs-lookup"><span data-stu-id="5521b-103">Network Redirectors</span></span>

<span data-ttu-id="5521b-104">Um redirecionador de rede é um driver de sistema de arquivos (ou FSD) que funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5521b-104">A network redirector is a file system driver (or FSD) that functions in the following manner:</span></span>

-   <span data-ttu-id="5521b-105">Como um cliente em uma operação de e/s de rede enviando solicitações de e/s para servidores e processando as respostas dos servidores.</span><span class="sxs-lookup"><span data-stu-id="5521b-105">As a client in a network I/O operation by sending I/O requests to servers and processing the responses from the servers.</span></span>
-   <span data-ttu-id="5521b-106">Como um servidor em uma operação de e/s de rede, recebendo solicitações de e/s de servidores e processando as solicitações.</span><span class="sxs-lookup"><span data-stu-id="5521b-106">As a server in a network I/O operation by receiving I/O requests from servers and processing the requests.</span></span>

<span data-ttu-id="5521b-107">Ele realiza toda a interação de nível baixo com o servidor para resolver o nome do arquivo fornecido pelo aplicativo com o local do recurso no servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="5521b-107">It performs all of the low-level interaction with the server in resolving the file name provided by the application with the location of the resource on the remote server.</span></span> <span data-ttu-id="5521b-108">Dessa forma, o redirecionador permite que o aplicativo acesse e manipule recursos em servidores remotos como se eles estivessem localizados no computador local.</span><span class="sxs-lookup"><span data-stu-id="5521b-108">In this way, the redirector enables the application to access and manipulate resources on remote servers as if they were located on the local machine.</span></span>

<span data-ttu-id="5521b-109">Os redirecionadores funcionam inteiramente no modo kernel.</span><span class="sxs-lookup"><span data-stu-id="5521b-109">Redirectors operate entirely within kernel mode.</span></span> <span data-ttu-id="5521b-110">Isso fornece as seguintes vantagens de desempenho em relação às alternativas de modo de usuário:</span><span class="sxs-lookup"><span data-stu-id="5521b-110">This provides the following performance advantages over user-mode alternatives:</span></span>

-   <span data-ttu-id="5521b-111">Ele pode interagir com FSDs de modo kernel em execução no servidor, como o servidor FSD, sem a necessidade de modo de usuário para kernel e alternâncias de contexto de modo kernel para usuário.</span><span class="sxs-lookup"><span data-stu-id="5521b-111">It can interact with kernel-mode FSDs running on the server, such as the server FSD, without the need for user-to-kernel mode and kernel-to-user mode context switches.</span></span>
-   <span data-ttu-id="5521b-112">Ele pode interagir no modo kernel com o Gerenciador de cache no servidor para armazenar em cache os dados de e/s enviados pelo Gerenciador de cache do servidor no cliente.</span><span class="sxs-lookup"><span data-stu-id="5521b-112">It can interact in kernel mode with the cache manager on the server to cache I/O data that the server cache manager sends on the client.</span></span>
-   <span data-ttu-id="5521b-113">As funções de API personalizadas feitas para solicitações de e/s remotas e as alterações nas funções de e/s de arquivo padrão para fornecer essa funcionalidade não são necessárias.</span><span class="sxs-lookup"><span data-stu-id="5521b-113">API functions custom-made for remote I/O requests, and changes to the standard file I/O functions to provide this functionality, are not necessary.</span></span>

 

 



