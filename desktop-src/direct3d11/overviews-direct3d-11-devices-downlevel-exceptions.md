---
title: Exceções
description: Este tópico descreve as exceções ao usar o Direct3D 11 em hardware de nível inferior.
ms.assetid: b3f85036-8572-40ee-b522-3b677443b840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97920ae42347cf618b22df82abc3b6e06bd5200d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294439"
---
# <a name="exceptions"></a>Exceções

Alguns recursos do Direct3D 11 não são totalmente especificados pelos níveis de recursos. Este tópico descreve as exceções ao usar o Direct3D 11 em hardware de nível inferior. Talvez um recurso tenha sido adicionado depois que o nível de recurso é definido (e requer um driver atualizado) ou, talvez, GPUs diferentes implementem implementações amplamente diferentes. As exceções de nível de recurso podem ser coletadas nos seguintes grupos:

-   [Formatos estendidos](#extended-formats)
-   [Suavização de multiamostras](#multisample-anti-aliasing)
-   [Tamanhos de Texture2D](#texture2d-sizes)
-   [Comportamento especial de adaptadores para o nível de recurso 9](#special-behavior-of-adapters-for-feature-level-9)
-   [Tópicos relacionados](#related-topics)

A seção de [referência do 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre o comportamento de vários métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) em vários níveis de recursos do 10Level9.

## <a name="extended-formats"></a>Formatos estendidos

Um formato estendido é um formato de pixel adicionado ao Direct3D 10,1 e ao Direct3D 11 para os níveis de recurso 10 \_ 0 e 10 \_ 1. Um formato estendido requer um driver atualizado (para o Direct3D 10 \_ 1 ou inferior). Use [**ID3D11Device:: CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) e [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) para consultar o suporte para esses formatos estendidos.

Um formato estendido:

-   Adiciona suporte para a ordem BGRA de recursos por componente de 8 bits.
-   Permite a conversão de um buffer de cadeia de permuta de valor inteiro. Isso permite que um aplicativo adicione ou remova o \_ sufixo sRGB ou renderize em uma \_ cadeia de permuta de polarização de XR.
-   Adiciona suporte opcional para o \_ formato dxgi \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM.
-   Garante que uma \_ \_ \_ cadeia de permuta flutuante de formato dxgi R16G16B16A16 seja apresentada como se os dados contidos não forem codificados por sRGB.

O conjunto completo de formatos estendidos tem suporte total ou não tem suporte, com exceção do formato de \_ polarização de XR. O \_ formato de polarização de XR é:

-   Sem suporte em qualquer nível de 9
-   Opcional no nível de 10 \_ 0 ou 10 \_ 1
-   Garantido no nível 11 \_ 0

## <a name="multisample-anti-aliasing"></a>Suavização de multiamostras

Implementações de MSAA têm pouca em comum em implementações de GPU. O nível de recurso 10,1 adicionou alguns mínimo bem definidos, mas em níveis de recursos inferiores, a MSAA deve ser testada explicitamente usando [**ID3D11Device:: CheckMultisampleQualityLevels**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkmultisamplequalitylevels).

## <a name="texture2d-sizes"></a>Tamanhos de Texture2D

Um nível de recurso garante que um tamanho mínimo possa ser criado, no entanto, um aplicativo pode criar texturas maiores até o tamanho total com suporte da GPU. Um aplicativo deve esperar falha de um método como [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) se um máximo for excedido.

## <a name="special-behavior-of-adapters-for-feature-level-9"></a>Comportamento especial de adaptadores para o nível de recurso 9

Os três níveis mais baixos de recursos do D3D \_ \_ nível \_ 9 \_ 1, nível de recurso do D3D \_ \_ \_ 9 \_ 2 e \_ \_ o nível de recurso do D3D \_ 9 \_ 3, compartilham uma DLL de implementação comum e tratam o argumento [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) para D3D11CreateDevice \[ AndSwapchain \] como um adaptador de modelo e criam seu próprio adaptador como parte da criação do dispositivo. Isso significa que o **IDXGIAdapter** passado para a rotina de criação não será o mesmo adaptador que foi recuperado do dispositivo por meio de IDXGIDevice:: getadapter. O impacto disso é que o **IDXGIOutputs** enumerado do adaptador passado não pode ser usado para entrar em tela inteira usando qualquer dispositivo de nível 9, já que essas saídas não pertencem ao adaptador do dispositivo. É uma boa prática descartar o adaptador de modelo passado e recuperar o adaptador criado do dispositivo usando IDXGIDevice:: getadapter, em que [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) pode ser recuperado usando QueryInterface da interface do dispositivo Direct3D.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct3D 11 em hardware de nível inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 