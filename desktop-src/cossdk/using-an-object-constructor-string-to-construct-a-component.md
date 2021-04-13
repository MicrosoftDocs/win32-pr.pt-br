---
description: Usando uma cadeia de caracteres de construtor de objeto para construir um componente
ms.assetid: 57d66988-2a65-4309-957a-36a5972233b5
title: Usando uma cadeia de caracteres de construtor de objeto para construir um componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cbbb1c156fd7ee675b6c21c8ae097494da59ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457047"
---
# <a name="using-an-object-constructor-string-to-construct-a-component"></a><span data-ttu-id="952dd-103">Usando uma cadeia de caracteres de construtor de objeto para construir um componente</span><span class="sxs-lookup"><span data-stu-id="952dd-103">Using an Object Constructor String to Construct a Component</span></span>

<span data-ttu-id="952dd-104">O exemplo a seguir ilustra como recuperar e usar programaticamente uma cadeia de caracteres de construtor de objeto quando um componente é instanciado.</span><span class="sxs-lookup"><span data-stu-id="952dd-104">The following example illustrates how to programmatically retrieve and use an object constructor string when a component is instantiated.</span></span> <span data-ttu-id="952dd-105">Ele mostra uma implementação da interface [**constructodeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) que recupera uma cadeia de caracteres de construtor de objeto.</span><span class="sxs-lookup"><span data-stu-id="952dd-105">It shows an implementation of the [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) interface that retrieves an object constructor string.</span></span> <span data-ttu-id="952dd-106">A cadeia de caracteres pode ser analisada para definir valores iniciais ou influenciar o comportamento do componente.</span><span class="sxs-lookup"><span data-stu-id="952dd-106">The string can then be parsed to set initial values or influence the behavior of the component.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="952dd-107">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="952dd-107">Visual Basic</span></span>


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="952dd-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="952dd-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="952dd-109">Conceitos de cadeias de caracteres do construtor de objeto COM+</span><span class="sxs-lookup"><span data-stu-id="952dd-109">COM+ Object Constructor Strings Concepts</span></span>](com--object-constructor-strings-concepts.md)
</dt> <dt>

[<span data-ttu-id="952dd-110">Especificando uma cadeia de caracteres de construtor de objeto para um componente</span><span class="sxs-lookup"><span data-stu-id="952dd-110">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



