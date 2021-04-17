---
title: Navegação por meio de teste de clique e local da tela
description: Para localizar os filhos de um objeto ou para determinar o tamanho de um objeto, os clientes podem clicar em pontos de teste na tela.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755875"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a><span data-ttu-id="da601-103">Navegação por meio de teste de clique e local da tela</span><span class="sxs-lookup"><span data-stu-id="da601-103">Navigation Through Hit Testing and Screen Location</span></span>

<span data-ttu-id="da601-104">Para localizar os filhos de um objeto ou para determinar o tamanho de um objeto, os clientes podem clicar em pontos de teste na tela.</span><span class="sxs-lookup"><span data-stu-id="da601-104">To locate an object's children or to determine an object's size, clients can hit test points on the screen.</span></span> <span data-ttu-id="da601-105">Dois métodos estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="da601-105">Two methods are available:</span></span>

-   [<span data-ttu-id="da601-106">**IAccessible:: accHitTest**</span><span class="sxs-lookup"><span data-stu-id="da601-106">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="da601-107">**IAccessible:: accLocation**</span><span class="sxs-lookup"><span data-stu-id="da601-107">**IAccessible::accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a><span data-ttu-id="da601-108">Usando IAccessible:: accHitTest</span><span class="sxs-lookup"><span data-stu-id="da601-108">Using IAccessible::accHitTest</span></span>

<span data-ttu-id="da601-109">Para identificar se um ponto está dentro de um objeto, dentro de seu filho ou nenhum deles, os clientes chamam o método [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) do objeto pai, passando as coordenadas da tela do ponto a ser testado.</span><span class="sxs-lookup"><span data-stu-id="da601-109">To identify whether a point is within an object, within its child, or neither, clients call the [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) method of the parent object, passing the screen coordinates of the point to be hit tested.</span></span> <span data-ttu-id="da601-110">A lista a seguir descreve alguns cenários típicos:</span><span class="sxs-lookup"><span data-stu-id="da601-110">The following list describes some typical scenarios:</span></span>

-   <span data-ttu-id="da601-111">Se os filhos do objeto se sobrepõem em um ponto especificado, [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) recupera o filho superior que parece Visual ocupar o espaço.</span><span class="sxs-lookup"><span data-stu-id="da601-111">If the object's children overlap at a specified point, [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) retrieves the topmost child that visually appears to occupy the space.</span></span>
-   <span data-ttu-id="da601-112">Se uma janela abranger um filho ou se o filho for recortado pelo pai, o teste de clique no ponto coberto recuperará o filho mesmo que ele não esteja visível.</span><span class="sxs-lookup"><span data-stu-id="da601-112">If a window covers a child, or if the child is clipped by the parent, hit testing the covered point retrieves the child even though it is not visible.</span></span>
-   <span data-ttu-id="da601-113">Se o filho encontrado no ponto especificado for um objeto acessível, em oposição a um elemento filho, o método retornará a interface [**IDispatch**](idispatch-interface.md) do filho.</span><span class="sxs-lookup"><span data-stu-id="da601-113">If the child found at the specified point is an accessible object, as opposed to a child element, the method returns the child's [**IDispatch**](idispatch-interface.md) interface.</span></span>

## <a name="using-iaccessibleacclocation"></a><span data-ttu-id="da601-114">Usando IAccessible:: accLocation</span><span class="sxs-lookup"><span data-stu-id="da601-114">Using IAccessible::accLocation</span></span>

<span data-ttu-id="da601-115">Para obter o local da tela de um objeto ou de um dos filhos do objeto, os clientes chamam [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span><span class="sxs-lookup"><span data-stu-id="da601-115">To get the screen location of an object or one of the object's children, clients call [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span></span> <span data-ttu-id="da601-116">Esse método retorna as coordenadas do retângulo delimitador do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="da601-116">This method returns the coordinates of the specified object's bounding rectangle.</span></span> <span data-ttu-id="da601-117">Se o objeto não estiver formatado como um retângulo, o método retornará as coordenadas do menor retângulo que abrange todo o objeto.</span><span class="sxs-lookup"><span data-stu-id="da601-117">If the object is not shaped like a rectangle, the method returns the coordinates of the smallest rectangle that encompasses the entire object.</span></span>

<span data-ttu-id="da601-118">A ilustração a seguir mostra a relação entre a região não retangular de um objeto e seu retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="da601-118">The following illustration shows the relationship between a non-rectangular object's region and its bounding rectangle.</span></span>

![ilustração mostrando a região de um objeto não retangular (um círculo) e seu retângulo delimitador.](images/region.gif)

> [!Note]  
> <span data-ttu-id="da601-120">[**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) é mais preciso que [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) porque permite que os clientes determinem o local de objetos em um pixel por pixel em vez de com retângulos delimitadores.</span><span class="sxs-lookup"><span data-stu-id="da601-120">[**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) is more precise than [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because it enables clients to determine the location of objects on a pixel-by-pixel basis rather than with bounding rectangles.</span></span> <span data-ttu-id="da601-121">Essa precisão é útil, por exemplo, quando um aplicativo está coletando informações rastreando o local do ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="da601-121">This precision is useful, for example, when an application is gathering information by tracking the location of the mouse pointer.</span></span>

 

 

 




