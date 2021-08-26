---
description: A funcionalidade a seguir foi adicionada à Microsoft DirectX Graphics Infrastructure (DXGI) 1,3, que está incluída a partir do Windows 8.1.
ms.assetid: 56816212-2B6A-41EC-B57D-29DEBBF440E7
title: Aprimoramentos de DXGI 1,3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709dc9e98ffe6ecd67f6bd91aa654b1e0bfe0375dabcd2a344f5b012c57dca2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984116"
---
# <a name="dxgi-13-improvements"></a>Aprimoramentos de DXGI 1,3

A funcionalidade a seguir foi adicionada à Microsoft DirectX Graphics Infrastructure (DXGI) 1,3, que está incluída a partir do Windows 8.1.

## <a name="trim-dxgi-adapter-memory-usage"></a>Cortar o uso de memória do adaptador DXGI

a partir do Windows 8.1, DXGI 1,3 adiciona a capacidade de liberar e liberar recursos de memória não utilizados alocados pelo adaptador DXGI. Isso permite que os aplicativos liberem a memória temporária ao suspender, reduzindo a chance de o aplicativo ser encerrado para liberar recursos para outros aplicativos. Quando o aplicativo for retomado, os drivers de dispositivo que dão suporte a Trim recriarão recursos conforme forem necessários. a partir de Windows 8.1, todos os dispositivos Direct3D criados por um aplicativo devem chamar [**IDXGIDevice3:: Trim**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgidevice3-trim) ao suspender para reduzir a superfície de memória e reduzir a chance de o aplicativo ser encerrado para recuperar recursos do sistema.

## <a name="multi-plane-overlays"></a>Sobreposições de vários planos

a partir do Windows 8.1, DXGI 1,3 dá suporte a sobreposições de vários planos. Você pode descobrir se o dispositivo dá suporte a sobreposições de vários planos no hardware usando [**IDXGIOutput2:: SupportsOverlays**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays).

## <a name="overlapping-swap-chains-and-swap-chain-scaling"></a>Sobrepondo cadeias de troca e dimensionamento de cadeia de permuta

a partir do Windows 8.1, DXGI 1,3 dá suporte a cadeias de troca sobrepostas. As cadeias de troca sobrepostas são usadas para desenhar gráficos 3D em resoluções não nativas (com upescalas de hardware) ao apresentar a interface do usuário na resolução nativa. Isso permite que os jogos aproveitem as taxas de preenchimento mais altas para a resposta a um jogo sem degradar a qualidade visual dos elementos da interface do usuário, como a Pontuação do jogador e o texto da caixa de diálogo. Em dispositivos que dão suporte a sobreposições de vários planos, o Direct3D usará sobreposições de vários planos para sobreposição de cadeias de troca. Crie uma cadeia de permuta em primeiro plano especificando o sinalizador de [**\_ \_ \_ \_ \_ camada de primeiro plano do sinalizador de cadeia de permuta dxgi**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) ao criar a cadeia de permuta e use [**IDXGISwapChain2:: SetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform) e [**IDXGISwapChain2:: GetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform) para dimensionar a cadeia de permuta usada para jogos.

## <a name="select-backbuffer-subregion-for-swap-chain"></a>Selecione a subregião de BackBuffer para a cadeia de permuta

a partir do Windows 8.1, DXGI 1,3 pode ser usado para selecionar uma subregião do backbuffer para uso com a cadeia de permuta, possibilitando o processamento para um buffer menor sem recriar a cadeia de permuta. Consulte [**IDXGISwapChain2:: Setsourceize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize) e [**IDXGISwapChain2:: getsourceize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getsourcesize).

## <a name="lower-latency-swap-chain-presentation"></a>Apresentação da cadeia de troca de latência mais baixa

a partir do Windows 8.1, DXGI 1,3 torna possível reduzir a latência, permitindo que a cadeia de permuta termine de apresentar o quadro anterior antes de começar a usar o dispositivo para desenhar o próximo quadro. Consulte [**IDXGISwapChain2:: GetFrameLatencyWaitableObject**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject), [**IDXGISwapChain2:: GetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency)e [**IDXGISwapChain2:: SetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency).

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
