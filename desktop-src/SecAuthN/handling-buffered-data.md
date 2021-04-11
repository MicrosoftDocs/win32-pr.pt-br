---
description: Várias das funções de provedor de rede pegam o endereço e o tamanho de um buffer no qual a função coloca uma estrutura de dados de tamanho variável.
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: Manipulando dados armazenados em buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e123fc1ccccae6120b6db1c9ada554acc5b02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170823"
---
# <a name="handling-buffered-data"></a><span data-ttu-id="7e7ac-103">Manipulando dados armazenados em buffer</span><span class="sxs-lookup"><span data-stu-id="7e7ac-103">Handling Buffered Data</span></span>

<span data-ttu-id="7e7ac-104">Várias das funções de provedor de rede pegam o endereço e o tamanho de um buffer no qual a função coloca uma estrutura de dados de tamanho variável.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-104">Several of the network provider functions take the address and size of a buffer into which the function places a variable-sized data structure.</span></span>

<span data-ttu-id="7e7ac-105">Em cada caso, o mecanismo usado é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-105">In each case, the mechanism used is the same.</span></span> <span data-ttu-id="7e7ac-106">O chamador aloca um buffer e passa seu endereço para a função.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-106">The caller allocates a buffer and passes its address to the function.</span></span> <span data-ttu-id="7e7ac-107">Ele também passa o endereço de um **DWORD** que especifica o tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-107">It also passes the address of a **DWORD** that specifies the size of the buffer, in bytes.</span></span>

<span data-ttu-id="7e7ac-108">Em seguida, a função copia o máximo da estrutura de dados solicitada como pode no buffer.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-108">The function then copies as much of the requested data structure as it can into the buffer.</span></span> <span data-ttu-id="7e7ac-109">Se todos os dados couberem no buffer, a função retornará o sucesso de WN \_ .</span><span class="sxs-lookup"><span data-stu-id="7e7ac-109">If all of the data fits into the buffer, the function returns WN\_SUCCESS.</span></span> <span data-ttu-id="7e7ac-110">Se os dados não couberem no buffer, os dados poderão ficar incompletos e a função definirá o \_ erro de mais dados do WN \_ .</span><span class="sxs-lookup"><span data-stu-id="7e7ac-110">If the data does not fit into the buffer, the data may be left incomplete, and the function sets the WN\_MORE\_DATA error.</span></span> <span data-ttu-id="7e7ac-111">Em ambos os casos, o **DWORD** que indica o tamanho do buffer é definido como o número de bytes realmente exigidos pela estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-111">In either case, the **DWORD** indicating the size of the buffer is set to the number of bytes actually required by the data structure.</span></span> <span data-ttu-id="7e7ac-112">Dessa forma, se o buffer passado era muito pequeno e a função falhou, o chamador pode alocar um novo buffer do tamanho necessário e chamar a função novamente.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-112">This way, if the buffer passed in was too small and the function failed, the caller may allocate a new buffer of the required size and call the function again.</span></span>

<span data-ttu-id="7e7ac-113">Quando as estruturas de dados retornadas incluem cadeias de caracteres de comprimento variável, as estruturas de dados individuais normalmente contêm ponteiros para essas cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-113">When the data structures returned include variable-length strings, the individual data structures typically contain pointers to these strings.</span></span> <span data-ttu-id="7e7ac-114">As cadeias de caracteres em si também devem ser colocadas dentro do buffer.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-114">The strings themselves should also be placed within the buffer.</span></span> <span data-ttu-id="7e7ac-115">No entanto, é importante colocá-los no final do buffer.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-115">However, it is important to place them at the end of the buffer.</span></span> <span data-ttu-id="7e7ac-116">Caso contrário, eles tornarão a indexação a enésimo estrutura impossível.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-116">Otherwise, they will make indexing to the Nth structure impossible.</span></span> <span data-ttu-id="7e7ac-117">Em outras palavras, todas as estruturas estão localizadas de forma contígua no início do buffer.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-117">In other words, all structures are located contiguously at the beginning of the buffer.</span></span> <span data-ttu-id="7e7ac-118">Ponteiros para cadeias de caracteres ou dados de comprimento variável devem ser ponteiros reais, não deslocamentos no buffer.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-118">Pointers to strings or variable length data must be actual pointers, not offsets into the buffer.</span></span>

<span data-ttu-id="7e7ac-119">Quando um buffer é usado para passar e retornar dados que consistem apenas em cadeias de caracteres, o **DWORD** que especifica o tamanho do buffer deve ser definido como o número total de personagens que se ajustarão a essas cadeias, não ao número de bytes.</span><span class="sxs-lookup"><span data-stu-id="7e7ac-119">When a buffer is used to pass in and return data that consists only of strings, the **DWORD** specifying the size of the buffer should be set to the total number of characters that will fit in these strings, not to the number of bytes.</span></span>

 

 



