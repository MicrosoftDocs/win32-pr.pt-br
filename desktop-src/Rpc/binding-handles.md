---
title: Identificadores de associação
description: A associação é o processo de criação de uma conexão lógica entre um programa cliente e um programa de servidor. As informações que compõem a associação entre o cliente e o servidor são representadas por uma estrutura chamada identificador de associação.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07973deb8319b44a82795a6402ef5e1a9310c2c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499064"
---
# <a name="binding-handles"></a><span data-ttu-id="492c3-104">Identificadores de associação</span><span class="sxs-lookup"><span data-stu-id="492c3-104">Binding Handles</span></span>

<span data-ttu-id="492c3-105">A associação é o processo de criação de uma conexão lógica entre um programa cliente e um programa de servidor.</span><span class="sxs-lookup"><span data-stu-id="492c3-105">Binding is the process of creating a logical connection between a client program and a server program.</span></span> <span data-ttu-id="492c3-106">As informações que compõem a associação entre o cliente e o servidor são representadas por uma estrutura chamada identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="492c3-106">The information that composes the binding between client and server is represented by a structure called a binding handle.</span></span>

<span data-ttu-id="492c3-107">Um identificador de associação é análogo a um identificador de arquivo que a função de biblioteca de tempo de execução fopen C retorna, ou um identificador de janela que a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) retorna.</span><span class="sxs-lookup"><span data-stu-id="492c3-107">A binding handle is analogous to a file handle that the fopen C run-time library function returns, or a window handle that the function [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) returns.</span></span>

<span data-ttu-id="492c3-108">Assim como acontece com esses identificadores, seu aplicativo não pode acessar e manipular diretamente as informações no identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="492c3-108">As with these handles, your application cannot directly access and manipulate the information in the binding handle.</span></span> <span data-ttu-id="492c3-109">As informações em uma estrutura de dados de identificador de associação estão disponíveis somente para as bibliotecas de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="492c3-109">The information in a binding handle data structure is available only to the RPC run-time libraries.</span></span> <span data-ttu-id="492c3-110">Você fornece o identificador, as bibliotecas de tempo de execução acessam e manipulam os dados apropriados.</span><span class="sxs-lookup"><span data-stu-id="492c3-110">You provide the handle, the run-time libraries access and manipulate the appropriate data.</span></span>

<span data-ttu-id="492c3-111">Esta seção apresenta uma discussão sobre identificadores de associação nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="492c3-111">This section presents a discussion on binding handles in the following topics:</span></span>

-   [<span data-ttu-id="492c3-112">Tipos de identificadores de associação</span><span class="sxs-lookup"><span data-stu-id="492c3-112">Types of Binding Handles</span></span>](types-of-binding-handles.md)
-   [<span data-ttu-id="492c3-113">Associação do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="492c3-113">Client-Side Binding</span></span>](client-side-binding.md)
-   [<span data-ttu-id="492c3-114">Associação do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="492c3-114">Server-Side Binding</span></span>](server-side-binding.md)
-   [<span data-ttu-id="492c3-115">Identificadores totalmente e parcialmente ligados</span><span class="sxs-lookup"><span data-stu-id="492c3-115">Fully and Partially Bound Handles</span></span>](fully-and-partially-bound-handles.md)
-   [<span data-ttu-id="492c3-116">Interpretando informações de associação</span><span class="sxs-lookup"><span data-stu-id="492c3-116">Interpreting Binding Information</span></span>](interpreting-binding-information.md)
-   [<span data-ttu-id="492c3-117">Extensões de Binding-Handle RPC da Microsoft</span><span class="sxs-lookup"><span data-stu-id="492c3-117">Microsoft RPC Binding-Handle Extensions</span></span>](microsoft-rpc-binding-handle-extensions.md)
-   [<span data-ttu-id="492c3-118">Funções de identificador de associação</span><span class="sxs-lookup"><span data-stu-id="492c3-118">Binding-Handle Functions</span></span>](binding-handle-functions.md)
-   [<span data-ttu-id="492c3-119">O banco de dados do serviço de nome RPC</span><span class="sxs-lookup"><span data-stu-id="492c3-119">The RPC Name Service Database</span></span>](the-rpc-name-service-database.md)

 

 