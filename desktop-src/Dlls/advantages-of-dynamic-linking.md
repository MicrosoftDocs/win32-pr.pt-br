---
description: A vinculação dinâmica tem as seguintes vantagens em relação à vinculação estática.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Vantagens da vinculação dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780549"
---
# <a name="advantages-of-dynamic-linking"></a><span data-ttu-id="c1748-103">Vantagens da vinculação dinâmica</span><span class="sxs-lookup"><span data-stu-id="c1748-103">Advantages of Dynamic Linking</span></span>

<span data-ttu-id="c1748-104">A vinculação dinâmica tem as seguintes vantagens em relação à vinculação estática:</span><span class="sxs-lookup"><span data-stu-id="c1748-104">Dynamic linking has the following advantages over static linking:</span></span>

-   <span data-ttu-id="c1748-105">Vários processos que carregam a mesma DLL no mesmo endereço base compartilham uma única cópia da DLL na memória física.</span><span class="sxs-lookup"><span data-stu-id="c1748-105">Multiple processes that load the same DLL at the same base address share a single copy of the DLL in physical memory.</span></span> <span data-ttu-id="c1748-106">Isso poupa a memória do sistema e reduz a permuta.</span><span class="sxs-lookup"><span data-stu-id="c1748-106">Doing this saves system memory and reduces swapping.</span></span>
-   <span data-ttu-id="c1748-107">Quando as funções em uma DLL são alteradas, os aplicativos que as usam não precisam ser recompilados ou vinculados desde que os argumentos da função, convenções de chamada e valores de retorno não sejam alterados.</span><span class="sxs-lookup"><span data-stu-id="c1748-107">When the functions in a DLL change, the applications that use them do not need to be recompiled or relinked as long as the function arguments, calling conventions, and return values do not change.</span></span> <span data-ttu-id="c1748-108">Por outro lado, o código do objeto vinculado estaticamente requer que o aplicativo seja vinculado novamente quando as funções forem alteradas.</span><span class="sxs-lookup"><span data-stu-id="c1748-108">In contrast, statically linked object code requires that the application be relinked when the functions change.</span></span>
-   <span data-ttu-id="c1748-109">Uma DLL pode fornecer suporte após o mercado.</span><span class="sxs-lookup"><span data-stu-id="c1748-109">A DLL can provide after-market support.</span></span> <span data-ttu-id="c1748-110">Por exemplo, uma DLL de driver de vídeo pode ser modificada para dar suporte a uma exibição que não estava disponível quando o aplicativo foi lançado inicialmente.</span><span class="sxs-lookup"><span data-stu-id="c1748-110">For example, a display driver DLL can be modified to support a display that was not available when the application was initially shipped.</span></span>
-   <span data-ttu-id="c1748-111">Programas escritos em linguagens de programação diferentes podem chamar a mesma função de DLL, desde que os programas sigam a mesma convenção de chamada usada pela função.</span><span class="sxs-lookup"><span data-stu-id="c1748-111">Programs written in different programming languages can call the same DLL function as long as the programs follow the same calling convention that the function uses.</span></span> <span data-ttu-id="c1748-112">A Convenção de chamada (como C, Pascal ou chamada padrão) controla a ordem na qual a função de chamada deve enviar os argumentos para a pilha, se a função ou a função de chamada é responsável por limpar a pilha e se os argumentos são passados em registros.</span><span class="sxs-lookup"><span data-stu-id="c1748-112">The calling convention (such as C, Pascal, or standard call) controls the order in which the calling function must push the arguments onto the stack, whether the function or the calling function is responsible for cleaning up the stack, and whether any arguments are passed in registers.</span></span> <span data-ttu-id="c1748-113">Para obter mais informações, consulte a documentação incluída no seu compilador.</span><span class="sxs-lookup"><span data-stu-id="c1748-113">For more information, see the documentation included with your compiler.</span></span>

<span data-ttu-id="c1748-114">Uma desvantagem potencial de usar DLLs é que o aplicativo não é independente; depende da existência de um módulo DLL separado.</span><span class="sxs-lookup"><span data-stu-id="c1748-114">A potential disadvantage to using DLLs is that the application is not self-contained; it depends on the existence of a separate DLL module.</span></span> <span data-ttu-id="c1748-115">O sistema encerra os processos usando a vinculação dinâmica em tempo de carregamento se eles exigem uma DLL que não foi encontrada na inicialização do processo e fornece uma mensagem de erro ao usuário.</span><span class="sxs-lookup"><span data-stu-id="c1748-115">The system terminates processes using load-time dynamic linking if they require a DLL that is not found at process startup and gives an error message to the user.</span></span> <span data-ttu-id="c1748-116">O sistema não encerra um processo usando vinculação dinâmica em tempo de execução nessa situação, mas as funções exportadas pela DLL ausente não estão disponíveis para o programa.</span><span class="sxs-lookup"><span data-stu-id="c1748-116">The system does not terminate a process using run-time dynamic linking in this situation, but functions exported by the missing DLL are not available to the program.</span></span>

 

 



