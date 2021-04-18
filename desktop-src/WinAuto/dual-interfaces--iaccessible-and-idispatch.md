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
# <a name="dual-interfaces-iaccessible-and-idispatch"></a>Interfaces duplas: IAccessible e IDispatch

Os desenvolvedores de servidor devem fornecer a interface COM (Standard Component Object Model) [**IDispatch**](idispatch-interface.md) para seus objetos acessíveis. A interface IDispatch permite que os aplicativos cliente escritos no Microsoft Visual Basic e várias linguagens de script usem os métodos e as propriedades expostos pelo [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Como um objeto acessível fornece acesso a um objeto indiretamente por meio de [IDispatch:: Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) ou diretamente com o **IAccessible**, ele é considerado com uma interface dupla.

Quando os clientes C/C++ retornam um ponteiro de interface IDispatch, os clientes podem chamar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para tentar converter o ponteiro da interface IDispatch em um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Para chamar os métodos **IAccessible** indiretamente, os clientes C/C++ chamam IDispatch:: Invoke. Para melhorar o desempenho, chame os métodos **IAccessible** para usar o objeto diretamente.

Para obter uma lista de IDs de expedição (DISPIDs) que o **IDispatch** usa para identificar os métodos e as propriedades do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , consulte o [Apêndice C: IAccessible DISPIDs](appendix-c--iaccessible-dispids.md).

> [!Note]  
> Na versão 2,0 e posterior do Microsoft Acessibilidade Ativa, os servidores não precisam implementar totalmente os métodos de [**IDispatch**](idispatch-interface.md) , mas podem simplesmente retornar E \_ NOTIMPL depois de inicializar quaisquer parâmetros de saída, conforme mostrado no exemplo a seguir.

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 