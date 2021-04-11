---
title: Monikers de classe
description: Embora as classes normalmente sejam identificadas diretamente com CLSIDs para funções como CoCreateInstance ou CoGetClassObject, as classes agora também podem ser identificadas com um moniker chamado de moniker de classe.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80886ce49ea25d2fb5acbf4dddf550c9d2c3ae29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292738"
---
# <a name="class-monikers"></a><span data-ttu-id="14633-103">Monikers de classe</span><span class="sxs-lookup"><span data-stu-id="14633-103">Class Monikers</span></span>

<span data-ttu-id="14633-104">Embora as classes normalmente sejam identificadas diretamente com CLSIDs para funções como [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), as classes agora também podem ser identificadas com um moniker chamado de *moniker de classe*.</span><span class="sxs-lookup"><span data-stu-id="14633-104">Although classes are typically identified directly with CLSIDs to functions such as [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), classes may also now be identified with a moniker called a *class moniker*.</span></span> <span data-ttu-id="14633-105">Os monikers de classe são associados ao objeto de classe da classe para a qual eles são criados.</span><span class="sxs-lookup"><span data-stu-id="14633-105">Class monikers bind to the class object of the class for which they are created.</span></span>

<span data-ttu-id="14633-106">A capacidade de identificar classes com um moniker dá suporte a operações úteis que, de outra forma, são difíceis.</span><span class="sxs-lookup"><span data-stu-id="14633-106">The ability to identify classes with a moniker supports useful operations that are otherwise unwieldy.</span></span> <span data-ttu-id="14633-107">Por exemplo, o arquivo monikers tradicionalmente suportava a ligação avançada somente para a classe associada à classe de arquivo à qual eles foram referenciados; um moniker para um arquivo do Excel se associaria a uma instância de um objeto do Excel, e um moniker a uma imagem GIF se associaria a uma instância do manipulador GIF registrado no momento.</span><span class="sxs-lookup"><span data-stu-id="14633-107">For example, file monikers traditionally supported rich binding only to the class associated with the class of file they referred to; a moniker to an Excel file would bind to an instance of an Excel object, and a moniker to a GIF image would bind to an instance of the currently registered GIF handler.</span></span> <span data-ttu-id="14633-108">Um moniker de classe permite que você indique a classe que deseja usar para manipular um arquivo por meio de composição com um moniker de arquivo.</span><span class="sxs-lookup"><span data-stu-id="14633-108">A class moniker allows you to indicate the class you want to use to manipulate a file through composition with a file moniker.</span></span> <span data-ttu-id="14633-109">Um moniker de classe para uma classe de gráfico 3D composta com um moniker para um arquivo do Excel produz um moniker que é associado a uma instância do objeto de gráfico 3D e inicializa o objeto com o conteúdo do arquivo do Excel.</span><span class="sxs-lookup"><span data-stu-id="14633-109">A class moniker for a 3D charting class composed with a moniker to an Excel file yields a moniker that binds to an instance of the 3D charting object and initializes the object with the contents of the Excel file.</span></span>

<span data-ttu-id="14633-110">Os monikers de classe são, portanto, mais úteis em composição com outros tipos de monikers, como moniker de arquivo ou monikers de item.</span><span class="sxs-lookup"><span data-stu-id="14633-110">Class monikers are therefore most useful in composition with other types of monikers, such as file monikers or item monikers.</span></span>

<span data-ttu-id="14633-111">Os monikers de classe também podem ser compostos à direita dos monikers que dão suporte à associação à interface [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) .</span><span class="sxs-lookup"><span data-stu-id="14633-111">Class monikers may also be composed to the right of monikers supporting binding to the [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) interface.</span></span> <span data-ttu-id="14633-112">Quando composta dessa maneira, **IClassActivator** simplesmente dá acesso ao objeto de classe e às instâncias da classe por meio de [**IClassActivator:: GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span><span class="sxs-lookup"><span data-stu-id="14633-112">When composed in this manner, **IClassActivator** simply gives access to the class object and instances of the class through [**IClassActivator::GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span></span> <span data-ttu-id="14633-113">Os monikers de classe podem ser identificados por meio de [**IMoniker:: IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), que retorna MKSYS \_ CLASSMONIKER em *pdwMksys*.</span><span class="sxs-lookup"><span data-stu-id="14633-113">Class monikers may be identified through [**IMoniker::IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), which returns MKSYS\_CLASSMONIKER in *pdwMksys*.</span></span>

<span data-ttu-id="14633-114">Os programadores normalmente criam monikers de classe usando a função [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) ou por meio de [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span><span class="sxs-lookup"><span data-stu-id="14633-114">Programmers typically create class monikers using the [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) function or through [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span></span> <span data-ttu-id="14633-115">(Consulte [**IMoniker::P arsedisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) para obter detalhes.)</span><span class="sxs-lookup"><span data-stu-id="14633-115">(See [**IMoniker::ParseDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) for details.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="14633-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14633-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14633-117">Anti-moniker</span><span class="sxs-lookup"><span data-stu-id="14633-117">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="14633-118">Monikers compostos</span><span class="sxs-lookup"><span data-stu-id="14633-118">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="14633-119">Monikers de arquivo</span><span class="sxs-lookup"><span data-stu-id="14633-119">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="14633-120">Monikers de item</span><span class="sxs-lookup"><span data-stu-id="14633-120">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="14633-121">Monikers de ponteiro</span><span class="sxs-lookup"><span data-stu-id="14633-121">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




