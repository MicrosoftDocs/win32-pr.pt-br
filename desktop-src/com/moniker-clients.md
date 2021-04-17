---
title: Clientes de moniker
description: Os clientes do moniker devem começar obtendo um moniker e há várias maneiras para um cliente moniker obter um moniker.
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761841"
---
# <a name="moniker-clients"></a><span data-ttu-id="3e436-103">Clientes de moniker</span><span class="sxs-lookup"><span data-stu-id="3e436-103">Moniker Clients</span></span>

<span data-ttu-id="3e436-104">Os clientes do moniker devem começar obtendo um moniker e há várias maneiras para um cliente moniker obter um moniker.</span><span class="sxs-lookup"><span data-stu-id="3e436-104">Moniker clients must start by getting a moniker, and there are several ways for a moniker client to get a moniker.</span></span> <span data-ttu-id="3e436-105">Por exemplo, em documentos compostos OLE, quando o usuário final cria um item vinculado (usando a caixa de diálogo **Inserir objeto** , a área de transferência ou arrasta e solta), um moniker é inserido como parte do item vinculado.</span><span class="sxs-lookup"><span data-stu-id="3e436-105">For example, in OLE compound documents, when the end user creates a linked item (either using **Insert Object** dialog, the clipboard, or drag-and drop), a moniker is embedded as part of the linked item.</span></span> <span data-ttu-id="3e436-106">Nesse caso, o programador tem um mínimo de contato com os monikers.</span><span class="sxs-lookup"><span data-stu-id="3e436-106">In that case, the programmer has minimal contact with monikers.</span></span> <span data-ttu-id="3e436-107">Programaticamente, se você tiver um ponteiro de interface para um objeto que implementa a interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , poderá usá-lo para obter um moniker, e existem métodos em outras interfaces que são definidas para retornar moniker.</span><span class="sxs-lookup"><span data-stu-id="3e436-107">Programmatically, if you have an interface pointer to an object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface, you can use that to get a moniker, and there are methods on other interfaces that are defined to return monikers.</span></span>

<span data-ttu-id="3e436-108">Há diferentes tipos de monikers, que são usados para identificar diferentes tipos de objetos, mas para um cliente moniker, todos os monikeres têm a mesma aparência.</span><span class="sxs-lookup"><span data-stu-id="3e436-108">There are different kinds of monikers, which are used to identify different kinds of objects, but to a moniker client, all monikers look the same.</span></span> <span data-ttu-id="3e436-109">Um cliente moniker simplesmente chama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) em um moniker e Obtém um ponteiro de interface para o objeto que o moniker identifica.</span><span class="sxs-lookup"><span data-stu-id="3e436-109">A moniker client simply calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on a moniker and gets an interface pointer to the object that the moniker identifies.</span></span> <span data-ttu-id="3e436-110">Se o moniker identificar um objeto tão grande quanto uma planilha inteira ou tão pequeno quanto uma única célula dentro de uma planilha, chamar **BindToObject** retornará um ponteiro para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="3e436-110">Whether the moniker identifies an object as large as an entire spreadsheet or as small as a single cell within a spreadsheet, calling **BindToObject** will return a pointer to that object.</span></span> <span data-ttu-id="3e436-111">Se o objeto já estiver em execução, o **BindToObject** irá encontrá-lo na memória.</span><span class="sxs-lookup"><span data-stu-id="3e436-111">If the object is already running, **BindToObject** will find it in memory.</span></span> <span data-ttu-id="3e436-112">Se o objeto for armazenado de forma passiva no disco, o **BindToObject** localizará um servidor para esse objeto, executará o servidor e fará com que o servidor Coloque o objeto no estado de execução.</span><span class="sxs-lookup"><span data-stu-id="3e436-112">If the object is stored passively on disk, **BindToObject** will locate a server for that object, run the server, and have the server bring the object into the running state.</span></span> <span data-ttu-id="3e436-113">Todos os detalhes do processo de associação estão ocultos do cliente moniker.</span><span class="sxs-lookup"><span data-stu-id="3e436-113">All the details of the binding process are hidden from the moniker client.</span></span> <span data-ttu-id="3e436-114">Portanto, para um cliente moniker, o uso do moniker é muito simples.</span><span class="sxs-lookup"><span data-stu-id="3e436-114">Thus, for a moniker client, using the moniker is very simple.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e436-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e436-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e436-116">Provedores de moniker</span><span class="sxs-lookup"><span data-stu-id="3e436-116">Moniker Providers</span></span>](moniker-providers.md)
</dt> <dt>

[<span data-ttu-id="3e436-117">Implementações de moniker OLE</span><span class="sxs-lookup"><span data-stu-id="3e436-117">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




