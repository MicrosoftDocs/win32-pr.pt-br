---
title: Como obter modos de exibição do adaptador
description: Este tópico mostra como usar a Microsoft DirectX Graphics Infrastructure (DXGI) para obter os modos de exibição válidos associados a um adaptador.
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c2602fcd4e1baa4476bb89273eda676f444e38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294084"
---
# <a name="how-to-get-adapter-display-modes"></a><span data-ttu-id="6deeb-103">Como: obter modos de exibição do adaptador</span><span class="sxs-lookup"><span data-stu-id="6deeb-103">How To: Get Adapter Display Modes</span></span>

<span data-ttu-id="6deeb-104">Este tópico mostra como usar a Microsoft DirectX Graphics Infrastructure (DXGI) para obter os modos de exibição válidos associados a um adaptador.</span><span class="sxs-lookup"><span data-stu-id="6deeb-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to get the valid display modes associated with an adapter.</span></span> <span data-ttu-id="6deeb-105">O DirectX 10 e 11 podem usar DXGI para obter os modos de exibição válidos.</span><span class="sxs-lookup"><span data-stu-id="6deeb-105">DirectX 10 and 11 can use DXGI to get the valid display modes.</span></span> <span data-ttu-id="6deeb-106">Conhecer os modos de exibição válidos garante que seu aplicativo possa escolher corretamente um modo de tela inteira válido.</span><span class="sxs-lookup"><span data-stu-id="6deeb-106">Knowing the valid display modes ensures that your application can properly choose a valid full-screen mode.</span></span>

<span data-ttu-id="6deeb-107">**Para obter modos de exibição do adaptador**</span><span class="sxs-lookup"><span data-stu-id="6deeb-107">**To get adapter display modes**</span></span>

1.  <span data-ttu-id="6deeb-108">Crie um objeto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) e use-o para enumerar os adaptadores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6deeb-108">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object and use it to enumerate the available adapters.</span></span> <span data-ttu-id="6deeb-109">Para obter mais informações, consulte [como: enumerar adaptadores](overviews-direct3d-11-devices-enum.md).</span><span class="sxs-lookup"><span data-stu-id="6deeb-109">For more information, see [How To: Enumerate Adapters](overviews-direct3d-11-devices-enum.md).</span></span>
2.  <span data-ttu-id="6deeb-110">Chame IDXGIAdapter:: EnumOutputs para enumerar as saídas de cada adaptador.</span><span class="sxs-lookup"><span data-stu-id="6deeb-110">Call IDXGIAdapter::EnumOutputs to enumerate the outputs for each adapter.</span></span>
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  <span data-ttu-id="6deeb-111">Chame IDXGIOutput:: getdisplaymodelist para recuperar uma matriz de [**estruturas \_ \_ desc de modo dxgi**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) e o número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="6deeb-111">Call IDXGIOutput::GetDisplayModeList to retrieve an array of [**DXGI\_MODE\_DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) structures and the number of elements in the array.</span></span> <span data-ttu-id="6deeb-112">Cada **estrutura \_ \_ desc de modo dxgi** representa um modo de exibição válido para a saída.</span><span class="sxs-lookup"><span data-stu-id="6deeb-112">Each **DXGI\_MODE\_DESC** structure represents a valid display mode for the output.</span></span>
    ```
    UINT numModes = 0;
    DXGI_MODE_DESC* displayModes = NULL;
    DXGI_FORMAT format = DXGI_FORMAT_R32G32B32A32_FLOAT;

        // Get the number of elements
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, NULL);

        displayModes = new DXGI_MODE_DESC[numModes]; 

        // Get the list
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, displayModes);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="6deeb-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6deeb-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6deeb-114">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="6deeb-114">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="6deeb-115">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="6deeb-115">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 