---
description: Quando o sistema inicia um programa que usa vinculação dinâmica em tempo de carregamento, ele usa as informações que o vinculador colocou no arquivo para localizar os nomes das DLLs usadas pelo processo.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Load-Time vinculação dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506181"
---
# <a name="load-time-dynamic-linking"></a><span data-ttu-id="6c445-103">Load-Time vinculação dinâmica</span><span class="sxs-lookup"><span data-stu-id="6c445-103">Load-Time Dynamic Linking</span></span>

<span data-ttu-id="6c445-104">Quando o sistema inicia um programa que usa vinculação dinâmica em tempo de carregamento, ele usa as informações que o vinculador colocou no arquivo para localizar os nomes das DLLs usadas pelo processo.</span><span class="sxs-lookup"><span data-stu-id="6c445-104">When the system starts a program that uses load-time dynamic linking, it uses the information the linker placed in the file to locate the names of the DLLs that are used by the process.</span></span> <span data-ttu-id="6c445-105">Em seguida, o sistema pesquisa as DLLs.</span><span class="sxs-lookup"><span data-stu-id="6c445-105">The system then searches for the DLLs.</span></span> <span data-ttu-id="6c445-106">Para obter mais informações, consulte [ordem de pesquisa da biblioteca de vínculo dinâmico](dynamic-link-library-search-order.md).</span><span class="sxs-lookup"><span data-stu-id="6c445-106">For more information, see [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).</span></span>

<span data-ttu-id="6c445-107">Se o sistema não puder localizar uma DLL necessária, ele encerrará o processo e exibirá uma caixa de diálogo que reportará o erro para o usuário.</span><span class="sxs-lookup"><span data-stu-id="6c445-107">If the system cannot locate a required DLL, it terminates the process and displays a dialog box that reports the error to the user.</span></span> <span data-ttu-id="6c445-108">Caso contrário, o sistema mapeia a DLL para o espaço de endereço virtual do processo e incrementa a contagem de referência de DLL.</span><span class="sxs-lookup"><span data-stu-id="6c445-108">Otherwise, the system maps the DLL into the virtual address space of the process and increments the DLL reference count.</span></span>

<span data-ttu-id="6c445-109">O sistema chama a função de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="6c445-109">The system calls the entry-point function.</span></span> <span data-ttu-id="6c445-110">A função recebe um código que indica que o processo está carregando a DLL.</span><span class="sxs-lookup"><span data-stu-id="6c445-110">The function receives a code indicating that the process is loading the DLL.</span></span> <span data-ttu-id="6c445-111">Se a função de ponto de entrada não retornar TRUE, o sistema encerrará o processo e relatará o erro.</span><span class="sxs-lookup"><span data-stu-id="6c445-111">If the entry-point function does not return TRUE, the system terminates the process and reports the error.</span></span> <span data-ttu-id="6c445-112">Para obter mais informações sobre a função de ponto de entrada, consulte [biblioteca de vínculo dinâmico Entry-Point função](dynamic-link-library-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="6c445-112">For more information about the entry-point function, see [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).</span></span>

<span data-ttu-id="6c445-113">Por fim, o sistema modifica a tabela de endereços de função com os endereços iniciais para as funções de DLL importadas.</span><span class="sxs-lookup"><span data-stu-id="6c445-113">Finally, the system modifies the function address table with the starting addresses for the imported DLL functions.</span></span>

<span data-ttu-id="6c445-114">A DLL é mapeada para o espaço de endereço virtual do processo durante sua inicialização e é carregada na memória física somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="6c445-114">The DLL is mapped into the virtual address space of the process during its initialization and is loaded into physical memory only when needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c445-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c445-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c445-116">Usando Load-Time vinculação dinâmica</span><span class="sxs-lookup"><span data-stu-id="6c445-116">Using Load-Time Dynamic Linking</span></span>](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



