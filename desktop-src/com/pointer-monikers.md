---
title: Monikers de ponteiro
description: Um moniker de ponteiro identifica um objeto que pode existir somente no estado ativo ou em execução. Isso difere de outras classes de monikers, que identificam objetos que podem existir no estado passivo ou ativo.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "104365438"
---
# <a name="pointer-monikers"></a><span data-ttu-id="f57f6-104">Monikers de ponteiro</span><span class="sxs-lookup"><span data-stu-id="f57f6-104">Pointer Monikers</span></span>

<span data-ttu-id="f57f6-105">Um *moniker de ponteiro* identifica um objeto que pode existir somente no estado ativo ou em execução.</span><span class="sxs-lookup"><span data-stu-id="f57f6-105">A *pointer moniker* identifies an object that can exist only in the active or running state.</span></span> <span data-ttu-id="f57f6-106">Isso difere de outras classes de monikers, que identificam objetos que podem existir no estado passivo ou ativo.</span><span class="sxs-lookup"><span data-stu-id="f57f6-106">This differs from other classes of monikers, which identify objects that can exist in either the passive or the active state.</span></span>

<span data-ttu-id="f57f6-107">Suponha, por exemplo, que um aplicativo tenha um objeto que não tenha nenhuma representação persistente.</span><span class="sxs-lookup"><span data-stu-id="f57f6-107">Suppose, for example, an application has an object that has no persistent representation.</span></span> <span data-ttu-id="f57f6-108">Normalmente, se um cliente do seu aplicativo precisar de acesso a esse objeto, você poderá simplesmente passar o cliente um ponteiro para o objeto.</span><span class="sxs-lookup"><span data-stu-id="f57f6-108">Normally, if a client of your application needs access to that object, you could simply pass the client a pointer to the object.</span></span> <span data-ttu-id="f57f6-109">No entanto, suponha que o cliente esteja esperando um moniker.</span><span class="sxs-lookup"><span data-stu-id="f57f6-109">However, suppose your client is expecting a moniker.</span></span> <span data-ttu-id="f57f6-110">Não é possível identificar o objeto com um moniker de arquivo, pois ele não está armazenado em um arquivo nem com um moniker de item, pois ele não está contido em outro objeto.</span><span class="sxs-lookup"><span data-stu-id="f57f6-110">The object cannot be identified with a file moniker, because it isn't stored in a file, nor with an item moniker, because it isn't contained in another object.</span></span>

<span data-ttu-id="f57f6-111">Em vez disso, seu aplicativo pode criar um moniker de ponteiro, que é um moniker que simplesmente contém um ponteiro internamente, e passá-lo para o cliente.</span><span class="sxs-lookup"><span data-stu-id="f57f6-111">Instead, your application can create a pointer moniker, which is a moniker that simply contains a pointer internally, and pass that to the client.</span></span> <span data-ttu-id="f57f6-112">O cliente pode tratar esse moniker como qualquer outro.</span><span class="sxs-lookup"><span data-stu-id="f57f6-112">The client can treat this moniker like any other.</span></span> <span data-ttu-id="f57f6-113">No entanto, quando o cliente chama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) no moniker do ponteiro, o código do moniker não verifica a tabela de objetos em execução (corrompidos) ou carrega qualquer coisa do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f57f6-113">However, when the client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on the pointer moniker, the moniker code does not check the running object table (ROT) or load anything from storage.</span></span> <span data-ttu-id="f57f6-114">Em vez disso, o código do moniker simplesmente chama [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro armazenado dentro do moniker.</span><span class="sxs-lookup"><span data-stu-id="f57f6-114">Instead, the moniker code simply calls [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer stored inside the moniker.</span></span>

<span data-ttu-id="f57f6-115">Os monikers de ponteiro permitem que os objetos existentes somente no estado ativo ou em execução participem de operações de moniker e sejam usados por clientes de moniker.</span><span class="sxs-lookup"><span data-stu-id="f57f6-115">Pointer monikers allow objects that exist only in the active or running state to participate in moniker operations and be used by moniker clients.</span></span> <span data-ttu-id="f57f6-116">Uma diferença importante entre os monikers do ponteiro e outras classes de moniker é que os monikers do ponteiro não podem ser salvos no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="f57f6-116">One important difference between pointer monikers and other classes of monikers is that pointer monikers cannot be saved to persistent storage.</span></span> <span data-ttu-id="f57f6-117">Se você fizer isso, chamar o método [**IMoniker:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f57f6-117">If you do, calling the [**IMoniker::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) method returns an error.</span></span> <span data-ttu-id="f57f6-118">Isso significa que os monikers de ponteiro são úteis apenas em situações especializadas.</span><span class="sxs-lookup"><span data-stu-id="f57f6-118">This means that pointer monikers are useful only in specialized situations.</span></span> <span data-ttu-id="f57f6-119">Você pode usar a função [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) se precisar usar um moniker de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="f57f6-119">You can use the [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) function if you need to use a pointer moniker.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f57f6-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f57f6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f57f6-121">Anti-moniker</span><span class="sxs-lookup"><span data-stu-id="f57f6-121">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="f57f6-122">Monikers de classe</span><span class="sxs-lookup"><span data-stu-id="f57f6-122">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="f57f6-123">Monikers compostos</span><span class="sxs-lookup"><span data-stu-id="f57f6-123">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="f57f6-124">Monikers de arquivo</span><span class="sxs-lookup"><span data-stu-id="f57f6-124">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="f57f6-125">Monikers de item</span><span class="sxs-lookup"><span data-stu-id="f57f6-125">Item Monikers</span></span>](item-monikers.md)
</dt> </dl>

 

 




