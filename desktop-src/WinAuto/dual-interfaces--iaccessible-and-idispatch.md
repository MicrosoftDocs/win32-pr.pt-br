---
title: Classes duplas IAccessible e IDispatch
description: Os desenvolvedores de servidor devem fornecer a interface COM (Standard Component Object Model) IDispatch para seus objetos acessíveis.
ms.assetid: 043d6777-6f9a-4e93-aadc-9cbe9a9119c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bbe19e35a04414253dc8f22c4edbc19a041b27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105814029"
---
# <a name="dual-interfaces-iaccessible-and-idispatch"></a><span data-ttu-id="47f9b-103">Interfaces duplas: IAccessible e IDispatch</span><span class="sxs-lookup"><span data-stu-id="47f9b-103">Dual Interfaces: IAccessible and IDispatch</span></span>

<span data-ttu-id="47f9b-104">Os desenvolvedores de servidor devem fornecer a interface COM (Standard Component Object Model) [**IDispatch**](idispatch-interface.md) para seus objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="47f9b-104">Server developers must provide the standard Component Object Model (COM) interface [**IDispatch**](idispatch-interface.md) for their accessible objects.</span></span> <span data-ttu-id="47f9b-105">A interface IDispatch permite que os aplicativos cliente escritos no Microsoft Visual Basic e várias linguagens de script usem os métodos e as propriedades expostos pelo [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="47f9b-105">The IDispatch interface allows client applications written in Microsoft Visual Basic and various scripting languages to use the methods and properties exposed by [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="47f9b-106">Como um objeto acessível fornece acesso a um objeto indiretamente por meio de [IDispatch:: Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) ou diretamente com o **IAccessible**, ele é considerado com uma interface dupla.</span><span class="sxs-lookup"><span data-stu-id="47f9b-106">Because an accessible object provides access to an object either indirectly through [IDispatch::Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) or directly with **IAccessible**, it is said to have a dual interface.</span></span>

<span data-ttu-id="47f9b-107">Quando os clientes C/C++ retornam um ponteiro de interface IDispatch, os clientes podem chamar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para tentar converter o ponteiro da interface IDispatch em um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="47f9b-107">When C/C++ clients get back an IDispatch interface pointer, clients can call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to try converting the IDispatch interface pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="47f9b-108">Para chamar os métodos **IAccessible** indiretamente, os clientes C/C++ chamam IDispatch:: Invoke.</span><span class="sxs-lookup"><span data-stu-id="47f9b-108">To call the **IAccessible** methods indirectly, C/C++ clients call IDispatch::Invoke.</span></span> <span data-ttu-id="47f9b-109">Para melhorar o desempenho, chame os métodos **IAccessible** para usar o objeto diretamente.</span><span class="sxs-lookup"><span data-stu-id="47f9b-109">For improved performance, call the **IAccessible** methods to use the object directly.</span></span>

<span data-ttu-id="47f9b-110">Para obter uma lista de IDs de expedição (DISPIDs) que o **IDispatch** usa para identificar os métodos e as propriedades do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , consulte o [Apêndice C: IAccessible DISPIDs](appendix-c--iaccessible-dispids.md).</span><span class="sxs-lookup"><span data-stu-id="47f9b-110">For a list of the dispatch IDs (DISPIDs) that **IDispatch** uses to identify the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties, see [Appendix C: IAccessible DISPIDs](appendix-c--iaccessible-dispids.md).</span></span>

> [!Note]  
> <span data-ttu-id="47f9b-111">Na versão 2,0 e posterior do Microsoft Acessibilidade Ativa, os servidores não precisam implementar totalmente os métodos de [**IDispatch**](idispatch-interface.md) , mas podem simplesmente retornar E \_ NOTIMPL depois de inicializar quaisquer parâmetros de saída, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="47f9b-111">Under version 2.0 and later of Microsoft Active Accessibility, servers do not have to fully implement the methods of [**IDispatch**](idispatch-interface.md) but can simply return E\_NOTIMPL after initializing any out parameters, as shown in the following example.</span></span>

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 