---
title: Como enumerar adaptadores
description: Este tópico mostra como usar o DXGI (infra-estrutura de gráficos do Microsoft DirectX) para enumerar os adaptadores gráficos disponíveis em um computador.
ms.assetid: f8ef981c-363e-4ac8-8734-69c68f346950
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af16aba0131d93a5f72732931a68f132126b5d48
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988683"
---
# <a name="how-to-enumerate-adapters"></a>Como enumerar adaptadores

Este tópico mostra como usar o DXGI (infra-estrutura de gráficos do Microsoft DirectX) para enumerar os adaptadores gráficos disponíveis em um computador. O Direct3D 10 e 11 podem usar DXGI para enumerar adaptadores.

Geralmente, você precisa enumerar adaptadores por estes motivos:

-   Para determinar quantos adaptadores gráficos são instalados em um computador.
-   Para ajudá-lo a escolher qual adaptador usar para criar um dispositivo Direct3D.
-   Para recuperar um objeto [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) que você pode usar para recuperar recursos do dispositivo.

**Para enumerar adaptadores**

1.  Crie um objeto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) chamando a função [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) . O exemplo de código a seguir demonstra como inicializar um objeto **IDXGIFactory** .
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  Enumere cada adaptador chamando o método [**IDXGIFactory:: EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) . O parâmetro *Adapter* permite especificar um número de índice com base em zero do adaptador a ser enumerado. Se nenhum adaptador estiver disponível no índice especificado, o método retornará o [**\_ erro dxgi \_ não \_ encontrado**](/windows/desktop/direct3ddxgi/dxgi-error).

    O exemplo de código a seguir demonstra como enumerar por meio dos adaptadores em um computador.

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

O exemplo de código a seguir demonstra como enumerar todos os adaptadores em um computador.

> [!Note]  
> Para o Direct3D 11,0 e posterior, recomendamos que os aplicativos sempre usem [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) e [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) em vez disso.

 


```C++
std::vector <IDXGIAdapter*> EnumerateAdapters(void)
{
    IDXGIAdapter * pAdapter; 
    std::vector <IDXGIAdapter*> vAdapters; 
    IDXGIFactory* pFactory = NULL; 
    

    // Create a DXGIFactory object.
    if(FAILED(CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)))
    {
        return vAdapters;
    }


    for ( UINT i = 0;
          pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND;
          ++i )
    {
        vAdapters.push_back(pAdapter); 
    } 


    if(pFactory)
    {
        pFactory->Release();
    }

    return vAdapters;

}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 