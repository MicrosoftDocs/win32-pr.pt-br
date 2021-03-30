---
title: Anti-moniker
description: O OLE fornece uma implementação de um tipo especial de moniker chamado de anti-moniker.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005657"
---
# <a name="anti-monikers"></a><span data-ttu-id="0f406-103">Anti-moniker</span><span class="sxs-lookup"><span data-stu-id="0f406-103">Anti-Monikers</span></span>

<span data-ttu-id="0f406-104">O OLE fornece uma implementação de um tipo especial de moniker chamado de *anti-moniker*.</span><span class="sxs-lookup"><span data-stu-id="0f406-104">OLE provides an implementation of a special type of moniker called an *anti-moniker*.</span></span> <span data-ttu-id="0f406-105">Você usa esse moniker na criação de novas classes moniker.</span><span class="sxs-lookup"><span data-stu-id="0f406-105">You use this moniker in the creation of new moniker classes.</span></span> <span data-ttu-id="0f406-106">Você o usa como o inverso do moniker no qual ele é composto, cancelando efetivamente esse moniker, praticamente da mesma forma que o operador ".." move um nível de diretório para cima em um comando do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="0f406-106">You use it as the inverse of the moniker that it is composed onto, effectively canceling that moniker, in much the same way that the ".." operator moves up a directory level in a file system command.</span></span>

<span data-ttu-id="0f406-107">É necessário ter um anti-moniker disponível, porque depois que um moniker composto é criado, não é possível excluir partes do moniker se, por exemplo, um objeto se mover.</span><span class="sxs-lookup"><span data-stu-id="0f406-107">It is necessary to have an anti-moniker available, because once a composite moniker is created, it is not possible to delete parts of the moniker if, for example, an object moves.</span></span> <span data-ttu-id="0f406-108">Em vez disso, você usa um anti-moniker para remover uma ou mais entradas de um moniker composto.</span><span class="sxs-lookup"><span data-stu-id="0f406-108">Instead, you use an anti-moniker to remove one or more entries from a composite moniker.</span></span>

<span data-ttu-id="0f406-109">Os antimonikers são uma classe moniker explicitamente destinada a uso como inverso.</span><span class="sxs-lookup"><span data-stu-id="0f406-109">Anti-monikers are a moniker class explicitly intended for use as an inverse.</span></span> <span data-ttu-id="0f406-110">COM define a função [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) nomeada, que retorna um anti-moniker.</span><span class="sxs-lookup"><span data-stu-id="0f406-110">COM defines the named [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) function, which returns an anti-moniker.</span></span> <span data-ttu-id="0f406-111">Geralmente, você usa essa função para implementar o método [**IMoniker:: inverso**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) .</span><span class="sxs-lookup"><span data-stu-id="0f406-111">You generally use this function to implement the [**IMoniker::Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) method.</span></span>

<span data-ttu-id="0f406-112">Um anti-moniker é apenas um inverso para esses tipos de moniker que são implementados para tratar os permonikers como inversos.</span><span class="sxs-lookup"><span data-stu-id="0f406-112">An anti-moniker is only an inverse for those types of monikers that are implemented to treat anti-monikers as an inverse.</span></span> <span data-ttu-id="0f406-113">Por exemplo, se você quiser remover a última parte de um moniker composto, não deverá criar um anti-moniker e Compose-lo no final da composição.</span><span class="sxs-lookup"><span data-stu-id="0f406-113">For example, if you want to remove the last piece of a composite moniker, you should not create an anti-moniker and compose it to the end of the composite.</span></span> <span data-ttu-id="0f406-114">Não é possível ter certeza de que a última parte da composição considera um antimoniker como inverso.</span><span class="sxs-lookup"><span data-stu-id="0f406-114">You cannot be sure that the last piece of the composite considers an anti-moniker to be its inverse.</span></span> <span data-ttu-id="0f406-115">Em vez disso, você deve chamar [**IMoniker:: enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) no moniker composto, especificando **false** como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0f406-115">Instead, you should call [**IMoniker::Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) on the composite moniker, specifying **FALSE** as the first parameter.</span></span> <span data-ttu-id="0f406-116">Isso cria um enumerador que retorna os moniker do componente na ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="0f406-116">This creates an enumerator that returns the component monikers in reverse order.</span></span> <span data-ttu-id="0f406-117">Use o enumerador para recuperar a última parte da composição e chame [**inversa**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) nesse moniker.</span><span class="sxs-lookup"><span data-stu-id="0f406-117">Use the enumerator to retrieve the last piece of the composite, and call [**Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) on that moniker.</span></span> <span data-ttu-id="0f406-118">O moniker retornado por **inverso** é o que você precisa para remover a última parte da composição.</span><span class="sxs-lookup"><span data-stu-id="0f406-118">The moniker returned by **Inverse** is what you need to remove the last piece of the composite.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f406-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f406-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f406-120">Monikers de classe</span><span class="sxs-lookup"><span data-stu-id="0f406-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="0f406-121">Monikers compostos</span><span class="sxs-lookup"><span data-stu-id="0f406-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="0f406-122">Monikers de arquivo</span><span class="sxs-lookup"><span data-stu-id="0f406-122">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="0f406-123">Monikers de item</span><span class="sxs-lookup"><span data-stu-id="0f406-123">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="0f406-124">Monikers de ponteiro</span><span class="sxs-lookup"><span data-stu-id="0f406-124">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




