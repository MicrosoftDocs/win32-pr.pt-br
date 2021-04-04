---
title: Movendo objetos
description: Movendo objetos
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, movendo objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007305"
---
# <a name="moving-objects"></a><span data-ttu-id="95248-104">Movendo objetos</span><span class="sxs-lookup"><span data-stu-id="95248-104">Moving Objects</span></span>

<span data-ttu-id="95248-105">Para mover um objeto em um domínio, use o método [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .</span><span class="sxs-lookup"><span data-stu-id="95248-105">To move an object within a domain, use the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="95248-106">**Para mover um objeto dentro de um domínio**</span><span class="sxs-lookup"><span data-stu-id="95248-106">**To move an object within a domain**</span></span>

1.  <span data-ttu-id="95248-107">Associar à interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) do objeto a ser movido.</span><span class="sxs-lookup"><span data-stu-id="95248-107">Bind to the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface of the object to move.</span></span>
2.  <span data-ttu-id="95248-108">Obtenha o ADsPath do objeto para mover da propriedade [**IADs. ADsPath**](/windows/desktop/ADSI/iads-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="95248-108">Get the ADsPath of the object to move from the [**IADs.ADsPath**](/windows/desktop/ADSI/iads-property-methods) property.</span></span>
3.  <span data-ttu-id="95248-109">Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) do contêiner para o qual o objeto será movido.</span><span class="sxs-lookup"><span data-stu-id="95248-109">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface of the container where the object will be moved to.</span></span>
4.  <span data-ttu-id="95248-110">Mova o objeto com o método [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .</span><span class="sxs-lookup"><span data-stu-id="95248-110">Move the object with the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="95248-111">Se existir uma interface para o objeto que foi movido, a interface não será válida depois que o objeto for movido, pois o objeto de diretório que a interface representa não existe mais.</span><span class="sxs-lookup"><span data-stu-id="95248-111">If an interface exists to the object that was moved, the interface is not valid after the object is moved because the directory object the interface represents no longer exists.</span></span>

<span data-ttu-id="95248-112">Para obter mais informações e um exemplo de código que mostra como mover um objeto, consulte [exemplo de código para mover um objeto](example-code-for-moving-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="95248-112">For more information and a code example that shows how to move an object, see [Example Code for Moving an Object](example-code-for-moving-an-object.md).</span></span>

 

 