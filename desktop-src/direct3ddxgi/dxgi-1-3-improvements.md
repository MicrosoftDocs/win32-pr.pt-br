---
description: A funcionalidade a seguir foi adicionada no Microsoft DirectX Graphic Infrastructure (DXGI) 1.3, que está incluído a partir do Windows 8.1.
ms.assetid: 56816212-2B6A-41EC-B57D-29DEBBF440E7
title: Melhorias do DXGI 1.3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709dc9e98ffe6ecd67f6bd91aa654b1e0bfe0375dabcd2a344f5b012c57dca2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984116"
---
# <a name="dxgi-13-improvements"></a>Melhorias do DXGI 1.3

A funcionalidade a seguir foi adicionada no Microsoft DirectX Graphic Infrastructure (DXGI) 1.3, que está incluído a partir do Windows 8.1.

## <a name="trim-dxgi-adapter-memory-usage"></a>Cortar o uso de memória do adaptador DXGI

A partir Windows 8.1, o DXGI 1.3 adiciona a capacidade de liberar e liberar recursos de memória não utilizados alocados pelo adaptador DXGI. Isso permite que os aplicativos liberem memória temporária durante a suspensão, reduzindo a chance de o aplicativo ser encerrado para liberar recursos para outros aplicativos. Quando o aplicativo for retomado, os drivers de dispositivo que deem suporte ao corte recriarão os recursos conforme necessário. A partir do Windows 8.1, todos os dispositivos Direct3D criados por um aplicativo devem chamar [**IDXGIDevice3::Trim**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgidevice3-trim) ao suspender para reduzir o espaço de memória e reduzir a chance de que o aplicativo seja encerrado para recuperar recursos do sistema.

## <a name="multi-plane-overlays"></a>Sobreposições de vários plano

A partir Windows 8.1, o DXGI 1.3 dá suporte a sobreposições de vários plano. Você pode descobrir se o dispositivo dá suporte a sobreposições de vários plano no hardware usando [**IDXGIOutput2::SupportsOverlays**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays).

## <a name="overlapping-swap-chains-and-swap-chain-scaling"></a>Sobreposição de cadeias de permuta e dimensionamento de cadeia de permuta

A partir do Windows 8.1, o DXGI 1.3 dá suporte a cadeias de troca sobrepostas. As cadeias de permuta sobrepostas são usadas para desenhar gráficos 3D em resoluções não nativas (com o upscaling de hardware) ao apresentar a interface do usuário na resolução nativa. Isso permite que os jogos aproveitem taxas de preenchimento mais altas para uma reprodução responsiva sem prejudicar a qualidade visual dos elementos da interface do usuário, como pontuação do jogador e texto da caixa de diálogo. Em dispositivos que suportam sobreposições de vários plano, o Direct3D usará sobreposições de vários plano para sobrepor cadeias de permuta. Crie uma cadeia de troca em primeiro plano especificando o sinalizador [**\_ \_ \_ \_ FOREGROUND \_ LAYER**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) DO SINALIZADOR DE CADEIA DE PERMUTA DXGI ao criar a cadeia de permuta e use [**IDXGISwapChain2::SetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform) e [**IDXGISwapChain2::GetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform) para dimensionar a cadeia de permuta usada para o jogo.

## <a name="select-backbuffer-subregion-for-swap-chain"></a>Selecione a sub-região de backbuffer para a cadeia de permuta

A partir do Windows 8.1, o DXGI 1.3 pode ser usado para selecionar uma sub-região do backbuffer para uso com a cadeia de permuta, possibilitando renderizar para um buffer de fundo menor sem recriar a cadeia de permuta. Consulte [**IDXGISwapChain2::SetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize) e [**IDXGISwapChain2::GetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getsourcesize).

## <a name="lower-latency-swap-chain-presentation"></a>Apresentação da cadeia de permuta de menor latência

A partir do Windows 8.1, o DXGI 1.3 possibilita reduzir a latência, deixando que a cadeia de permuta termine de apresentar o quadro anterior antes de começar a usar o dispositivo para desenhar o próximo quadro. Consulte [**IDXGISwapChain2::GetFrameLatencyWaitableObject**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject), [**IDXGISwapChain2::GetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency)e [**IDXGISwapChain2::SetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency).

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
