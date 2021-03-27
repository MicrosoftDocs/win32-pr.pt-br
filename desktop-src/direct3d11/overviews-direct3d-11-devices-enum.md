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
# <a name="how-to-enumerate-adapters"></a><span data-ttu-id="8930d-103">Como enumerar adaptadores</span><span class="sxs-lookup"><span data-stu-id="8930d-103">How To: Enumerate Adapters</span></span>

<span data-ttu-id="8930d-104">Este tópico mostra como usar o DXGI (infra-estrutura de gráficos do Microsoft DirectX) para enumerar os adaptadores gráficos disponíveis em um computador.</span><span class="sxs-lookup"><span data-stu-id="8930d-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to enumerate the available graphics adapters on a computer.</span></span> <span data-ttu-id="8930d-105">O Direct3D 10 e 11 podem usar DXGI para enumerar adaptadores.</span><span class="sxs-lookup"><span data-stu-id="8930d-105">Direct3D 10 and 11 can use DXGI to enumerate adapters.</span></span>

<span data-ttu-id="8930d-106">Geralmente, você precisa enumerar adaptadores por estes motivos:</span><span class="sxs-lookup"><span data-stu-id="8930d-106">You generally need to enumerate adapters for these reasons:</span></span>

-   <span data-ttu-id="8930d-107">Para determinar quantos adaptadores gráficos são instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="8930d-107">To determine how many graphics adapters are installed on a computer.</span></span>
-   <span data-ttu-id="8930d-108">Para ajudá-lo a escolher qual adaptador usar para criar um dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8930d-108">To help you choose which adapter to use to create a Direct3D device.</span></span>
-   <span data-ttu-id="8930d-109">Para recuperar um objeto [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) que você pode usar para recuperar recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8930d-109">To retrieve an [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) object that you can use to retrieve device capabilities.</span></span>

<span data-ttu-id="8930d-110">**Para enumerar adaptadores**</span><span class="sxs-lookup"><span data-stu-id="8930d-110">**To enumerate adapters**</span></span>

1.  <span data-ttu-id="8930d-111">Crie um objeto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) chamando a função [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) .</span><span class="sxs-lookup"><span data-stu-id="8930d-111">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object by calling the [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) function.</span></span> <span data-ttu-id="8930d-112">O exemplo de código a seguir demonstra como inicializar um objeto **IDXGIFactory** .</span><span class="sxs-lookup"><span data-stu-id="8930d-112">The following code example demonstrates how to initialize an **IDXGIFactory** object.</span></span>
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  <span data-ttu-id="8930d-113">Enumere cada adaptador chamando o método [**IDXGIFactory:: EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) .</span><span class="sxs-lookup"><span data-stu-id="8930d-113">Enumerate through each adapter by calling the [**IDXGIFactory::EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) method.</span></span> <span data-ttu-id="8930d-114">O parâmetro *Adapter* permite especificar um número de índice com base em zero do adaptador a ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="8930d-114">The *Adapter* parameter allows you to specify a zero-based index number of the adapter to enumerate.</span></span> <span data-ttu-id="8930d-115">Se nenhum adaptador estiver disponível no índice especificado, o método retornará o [**\_ erro dxgi \_ não \_ encontrado**](/windows/desktop/direct3ddxgi/dxgi-error).</span><span class="sxs-lookup"><span data-stu-id="8930d-115">If no adapter is available at the specified index, the method returns [**DXGI\_ERROR\_NOT\_FOUND**](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>

    <span data-ttu-id="8930d-116">O exemplo de código a seguir demonstra como enumerar por meio dos adaptadores em um computador.</span><span class="sxs-lookup"><span data-stu-id="8930d-116">The following code example demonstrates how to enumerate through the adapters on a computer.</span></span>

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

<span data-ttu-id="8930d-117">O exemplo de código a seguir demonstra como enumerar todos os adaptadores em um computador.</span><span class="sxs-lookup"><span data-stu-id="8930d-117">The following code example demonstrates how to enumerate all adapters on a computer.</span></span>

> [!Note]  
> <span data-ttu-id="8930d-118">Para o Direct3D 11,0 e posterior, recomendamos que os aplicativos sempre usem [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) e [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="8930d-118">For Direct3D 11.0 and later, we recommend that apps always use [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) and [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) instead.</span></span>

 


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



## <a name="related-topics"></a><span data-ttu-id="8930d-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8930d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8930d-120">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="8930d-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 