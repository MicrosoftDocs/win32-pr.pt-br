---
description: Descreve como inicializar um OM XPS, que permite a um programa criar um documento XPS.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Inicializar um OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac44a69d171c1d38633512b0e275dcdeaea8738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296615"
---
# <a name="initialize-an-xps-om"></a><span data-ttu-id="d8c78-103">Inicializar um OM XPS</span><span class="sxs-lookup"><span data-stu-id="d8c78-103">Initialize an XPS OM</span></span>

<span data-ttu-id="d8c78-104">Descreve como inicializar um OM XPS, que permite a um programa criar um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="d8c78-104">Describes how to initialize an XPS OM, which allows a program to create an XPS document.</span></span>

<span data-ttu-id="d8c78-105">As interfaces da API do documento XPS são criadas por uma interface [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) .</span><span class="sxs-lookup"><span data-stu-id="d8c78-105">The interfaces of the XPS Document API are created by an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface.</span></span> <span data-ttu-id="d8c78-106">Para obter um ponteiro para um **IXpsOMObjectFactory** que possa ser usado em seu programa, chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="d8c78-106">To obtain a pointer to an **IXpsOMObjectFactory** that can be used in your program, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="d8c78-107">Antes de usar os exemplos de código a seguir em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d8c78-107">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="d8c78-108">Exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d8c78-108">Code Example</span></span>

<span data-ttu-id="d8c78-109">O exemplo a seguir cria a fábrica de objetos que será usada para criar interfaces de OM XPS em outros exemplos.</span><span class="sxs-lookup"><span data-stu-id="d8c78-109">The following example creates the object factory that will be used to create XPS OM interfaces in other examples.</span></span>


```C++
    IXpsOMObjectFactory *xpsFactory;

    HRESULT hr = S_OK;

    // Init COM for this thread if it hasn't 
    //  been initialized, yet.
    hr = CoInitializeEx(0, COINIT_MULTITHREADED);

    hr = CoCreateInstance(
        __uuidof(XpsOMObjectFactory),
        NULL, 
        CLSCTX_INPROC_SERVER,
        __uuidof(IXpsOMObjectFactory),
        reinterpret_cast<LPVOID*>(&xpsFactory));

    if (SUCCEEDED(hr))
    {
        // Make sure that you got a pointer 
        //  to the interface.

        // Use object factory...

        // ... and release when done
        xpsFactory->Release();
    }

    // Uninitialize COM when finished
    CoUninitialize();
```



## <a name="best-practices"></a><span data-ttu-id="d8c78-110">Práticas Recomendadas</span><span class="sxs-lookup"><span data-stu-id="d8c78-110">Best Practices</span></span>

<span data-ttu-id="d8c78-111">Você pode tornar seu programa mais eficiente obtendo um ponteiro para uma interface [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) na primeira vez que precisar chamar **IXpsOMObjectFactory** para criar uma interface e, em seguida, salvar o ponteiro para uso em outras áreas do programa.</span><span class="sxs-lookup"><span data-stu-id="d8c78-111">You can make your program more efficient by obtaining a pointer to an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface the first time that you need to call **IXpsOMObjectFactory** to create an interface, and then saving the pointer for use in other areas of the program.</span></span> <span data-ttu-id="d8c78-112">Quando o programa não precisar mais da fábrica de objetos ou não precisar dela por um tempo, o ponteiro poderá ser liberado.</span><span class="sxs-lookup"><span data-stu-id="d8c78-112">When the program no longer needs the object factory, or will not need it for a while, the pointer can be released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8c78-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8c78-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d8c78-114">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="d8c78-114">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="d8c78-115">Criar um OM XPS em branco</span><span class="sxs-lookup"><span data-stu-id="d8c78-115">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)
</dt> <dt>

<span data-ttu-id="d8c78-116">**Usado nesta seção**</span><span class="sxs-lookup"><span data-stu-id="d8c78-116">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="d8c78-117">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="d8c78-117">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="d8c78-118">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="d8c78-118">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

<span data-ttu-id="d8c78-119">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="d8c78-119">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="d8c78-120">Empacotamento</span><span class="sxs-lookup"><span data-stu-id="d8c78-120">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="d8c78-121">Referência da API do documento XPS</span><span class="sxs-lookup"><span data-stu-id="d8c78-121">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="d8c78-122">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="d8c78-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
