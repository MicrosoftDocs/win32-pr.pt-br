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
# <a name="how-to-get-adapter-display-modes"></a>Como: obter modos de exibição do adaptador

Este tópico mostra como usar a Microsoft DirectX Graphics Infrastructure (DXGI) para obter os modos de exibição válidos associados a um adaptador. O DirectX 10 e 11 podem usar DXGI para obter os modos de exibição válidos. Conhecer os modos de exibição válidos garante que seu aplicativo possa escolher corretamente um modo de tela inteira válido.

**Para obter modos de exibição do adaptador**

1.  Crie um objeto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) e use-o para enumerar os adaptadores disponíveis. Para obter mais informações, consulte [como: enumerar adaptadores](overviews-direct3d-11-devices-enum.md).
2.  Chame IDXGIAdapter:: EnumOutputs para enumerar as saídas de cada adaptador.
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  Chame IDXGIOutput:: getdisplaymodelist para recuperar uma matriz de [**estruturas \_ \_ desc de modo dxgi**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) e o número de elementos na matriz. Cada **estrutura \_ \_ desc de modo dxgi** representa um modo de exibição válido para a saída.
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

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 