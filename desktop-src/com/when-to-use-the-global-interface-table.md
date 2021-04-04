---
title: Quando usar a tabela de interface global
description: Quando usar a tabela de interface global
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008409"
---
# <a name="when-to-use-the-global-interface-table"></a><span data-ttu-id="4e192-103">Quando usar a tabela de interface global</span><span class="sxs-lookup"><span data-stu-id="4e192-103">When to Use the Global Interface Table</span></span>

<span data-ttu-id="4e192-104">Se você estiver desempacotando um ponteiro de interface várias vezes entre Apartments em um processo, você poderá usar a interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="4e192-104">If you are unmarshaling an interface pointer multiple times between apartments in a process, you might use the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="4e192-105">Com outras técnicas, você precisaria fazer o reempacotamento a cada vez.</span><span class="sxs-lookup"><span data-stu-id="4e192-105">With other techniques, you would have to remarshal each time.</span></span>

> [!Note]  
> <span data-ttu-id="4e192-106">Se o ponteiro de interface não tiver marshaling apenas uma vez, talvez você queira usar a função [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) .</span><span class="sxs-lookup"><span data-stu-id="4e192-106">If the interface pointer is unmarshaled only once, you may want to use the [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) function.</span></span> <span data-ttu-id="4e192-107">Ele também pode ser usado para passar um ponteiro de interface de um thread para outro thread no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="4e192-107">It can also be used to pass an interface pointer from one thread to another thread in the same process.</span></span>

 

<span data-ttu-id="4e192-108">A interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) também torna mais simples o problema anteriormente mais difícil para o programador.</span><span class="sxs-lookup"><span data-stu-id="4e192-108">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface also makes another previously difficult problem simpler for the programmer.</span></span> <span data-ttu-id="4e192-109">Esse problema ocorre quando as seguintes condições se aplicam:</span><span class="sxs-lookup"><span data-stu-id="4e192-109">This problem occurs when the following conditions apply:</span></span>

-   <span data-ttu-id="4e192-110">Um objeto ágil no processo agrega o marshaler de thread livre.</span><span class="sxs-lookup"><span data-stu-id="4e192-110">An in-process agile object aggregates the free-threaded marshaler.</span></span>
-   <span data-ttu-id="4e192-111">Esse mesmo objeto Agile também contém ponteiros de interface (como variáveis de membro) para outros objetos que não são ágeis e não agregam o marshaler de thread livre.</span><span class="sxs-lookup"><span data-stu-id="4e192-111">This same agile object also holds (as member variables) interface pointers to other objects that are not agile and do not aggregate the free-threaded marshaler.</span></span>

<span data-ttu-id="4e192-112">Nessa situação, se o objeto externo for empacotado para outro apartamento e o aplicativo for chamado, e o objeto tentar chamar em qualquer um de seus ponteiros de interface de variável de membro que não sejam de thread livre ou que sejam proxies para objetos em outros Apartments, poderá obter resultados incorretos ou o thread de erro RPC \_ E \_ incorreto \_ .</span><span class="sxs-lookup"><span data-stu-id="4e192-112">In this situation, if the outer object gets marshaled to another apartment and the application calls on it, and the object tries to call on any of its member variable interface pointers that are not free-threaded or are proxies to objects in other apartments, it might get incorrect results or the error RPC\_E\_WRONG\_THREAD.</span></span> <span data-ttu-id="4e192-113">Esse erro ocorre porque a interface interna foi projetada para ser chamada somente do apartamento no qual ela foi armazenada pela primeira vez na variável de membro.</span><span class="sxs-lookup"><span data-stu-id="4e192-113">This error occurs because the inner interface is designed to be callable only from the apartment in which it was first stored in the member variable.</span></span>

<span data-ttu-id="4e192-114">Para resolver esse problema, o objeto externo que agrega o marshaler de thread livre deve chamar [**IGlobalInterfaceTable:: RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) na interface interna e armazenar o cookie resultante em sua variável de membro, em vez de armazenar o ponteiro de interface real.</span><span class="sxs-lookup"><span data-stu-id="4e192-114">To solve this problem, the outer object aggregating the free-threaded marshaler should call [**IGlobalInterfaceTable::RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) on the inner interface and store the resulting cookie in its member variable, instead of storing the actual interface pointer.</span></span> <span data-ttu-id="4e192-115">Quando o objeto externo deseja chamar em um ponteiro de interface do objeto interno, ele deve chamar [**IGlobalInterfaceTable:: GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), usar o ponteiro de interface retornado e, em seguida, liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="4e192-115">When the outer object wants to call on an inner object's interface pointer, it should call [**IGlobalInterfaceTable::GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), use the returned interface pointer, and then release it.</span></span> <span data-ttu-id="4e192-116">Quando o objeto externo desaparece, ele deve chamar [**IGlobalInterfaceTable:: RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) para remover a interface da tabela de interface global.</span><span class="sxs-lookup"><span data-stu-id="4e192-116">When the outer object goes away, it should call [**IGlobalInterfaceTable::RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) to remove the interface from the global interface table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e192-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e192-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e192-118">Criando a tabela de interface global</span><span class="sxs-lookup"><span data-stu-id="4e192-118">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
</dt> </dl>

 

 