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
# <a name="initialize-an-xps-om"></a>Inicializar um OM XPS

Descreve como inicializar um OM XPS, que permite a um programa criar um documento XPS.

As interfaces da API do documento XPS são criadas por uma interface [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) . Para obter um ponteiro para um **IXpsOMObjectFactory** que possa ser usado em seu programa, chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

Antes de usar os exemplos de código a seguir em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de documentos XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Exemplo de código

O exemplo a seguir cria a fábrica de objetos que será usada para criar interfaces de OM XPS em outros exemplos.


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



## <a name="best-practices"></a>Práticas Recomendadas

Você pode tornar seu programa mais eficiente obtendo um ponteiro para uma interface [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) na primeira vez que precisar chamar **IXpsOMObjectFactory** para criar uma interface e, em seguida, salvar o ponteiro para uso em outras áreas do programa. Quando o programa não precisar mais da fábrica de objetos ou não precisar dela por um tempo, o ponteiro poderá ser liberado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Próximas etapas**
</dt> <dt>

[Criar um OM XPS em branco](create-a-blank-xps-om.md)
</dt> <dt>

**Usado nesta seção**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

**Para obter mais informações**
</dt> <dt>

[Empacotamento](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Referência da API do documento XPS](xps-programming-reference.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
