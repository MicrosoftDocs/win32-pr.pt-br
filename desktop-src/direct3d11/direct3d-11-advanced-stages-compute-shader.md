---
title: Visão geral do sombreador de computação
description: Um sombreador de computação é um estágio de sombreador programável que expande o Microsoft Direct3D 11 além da programação de gráficos. A tecnologia de sombreador de computação também é conhecida como a tecnologia DirectCompute.
ms.assetid: 02c1f98e-fdd6-49b0-b8b2-efbd472ab599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c890e63b468a993e0d08f678d2276d6ce2adad
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103642963"
---
# <a name="compute-shader-overview"></a>Visão geral do sombreador de computação

Um sombreador de computação é um estágio de sombreador programável que expande o Microsoft Direct3D 11 além da programação de gráficos. A tecnologia de sombreador de computação também é conhecida como a tecnologia DirectCompute.

Como outros sombreadores programáveis (por exemplo, sombreadores de vértice e de geometria), um sombreador de computação é projetado e implementado com [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) , mas isso é quase onde termina a similaridade. Um sombreador de computação fornece a computação alta velocidade de finalidade geral e tira proveito de um grande número de processadores paralelos na unidade de processamento gráfico (GPU). O estágio do sombreador de cálculo fornece compartilhamento de memória e sincronização de thread para permitir métodos mais eficazes de programação paralelos. Você chama o método [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) ou [**ID3D11DeviceContext::D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect) para executar comandos em um sombreador de computação. Um sombreador de computação pode ser executado em vários threads em paralelo.

## <a name="using-compute-shader-on-direct3d-10x-hardware"></a>Usando o sombreador de computação no hardware do Direct3D 10. x

Um sombreador de computação no Microsoft Direct3D 10 também é conhecido como DirectCompute 4. x.

Se você usar a API do Direct3D 11 e os drivers atualizados, o hardware do Direct3D de [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) 10 e 10,1 pode, opcionalmente, dar suporte a uma forma limitada de DirectCompute que usa os \_ perfis CS 4 \_ 0 e cs \_ 4 \_ 1. [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models) Ao usar o DirectCompute nesse hardware, tenha em mente as seguintes limitações:

-   O número máximo de threads é limitado ao \_ \_ grupo de threads D3D11 CS 4 \_ X máximo de \_ \_ \_ \_ threads \_ por \_ grupo (768) por grupo.
-   A dimensão X e Y de **numthreads** é limitada a D3D11 \_ cs \_ 4 \_ x \_ thread \_ Group \_ Max \_ x (768) e D3D11 \_ cs \_ 4 \_ x \_ thread \_ Group \_ Max \_ Y (768).
-   A dimensão Z de **numthreads** é limitada a 1.
-   A dimensão Z de expedição é limitada a D3D11 \_ cs \_ 4 \_ X \_ expedição \_ máxima \_ \_ grupos de threads \_ na \_ \_ dimensão Z (1).
-   Somente uma exibição de acesso não ordenado pode ser associada ao sombreador (D3D11 \_ cs \_ 4 \_ X \_ UAV \_ Register \_ Count é 1).
-   Somente [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s e [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s estão disponíveis como modos de exibição de acesso não ordenado.
-   Um thread só pode acessar sua própria região na memória groupshared para gravação, embora possa ser lido em qualquer local.
-   [VA \_ GroupIndex](/previous-versions/windows/desktop/legacy/ff471569(v=vs.85)) ou [ \_ DispatchThreadID VA](/windows/desktop/direct3dhlsl/sv-dispatchthreadid) deve ser usado ao acessar a memória **groupshared** para gravação.
-   A memória **Groupshared** é limitada a 16 KB por grupo.
-   Um único thread é limitado a uma região de 256 bytes de memória **groupshared** para gravação.
-   Não há instruções atômicas disponíveis.
-   Não há valores de precisão dupla disponíveis.

## <a name="using-compute-shader-on-direct3d-11x-hardware"></a>Usando o sombreador de computação no hardware do Direct3D 11. x

Um sombreador de computação no Direct3D 11 também é conhecido como DirectCompute 5,0.

Ao usar o DirectCompute com \_ perfis cs \_ 5 [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models)0, tenha em mente os seguintes itens:

-   O número máximo de threads é limitado ao \_ \_ grupo de threads D3D11 cs máximo de \_ \_ \_ threads \_ por \_ grupo (1024) por grupo.
-   A dimensão X e Y de **numthreads** é limitada ao \_ grupo de \_ threads cs D3D11 \_ \_ Max \_ X (1024) e D3D11 \_ cs \_ \_ Group thread \_ Max \_ Y (1024).
-   A dimensão Z de **numthreads** é limitada ao \_ grupo de \_ threads cs D3D11 \_ \_ Max \_ Z (64).
-   A dimensão máxima de expedição é limitada aos grupos de threads máximos de expedição do D3D11 \_ cs \_ \_ \_ \_ \_ por \_ dimensão (65535).
-   O número máximo de exibições de acesso não ordenado que podem ser associadas a um sombreador é D3D11 \_ PS \_ cs \_ UAV \_ registrar \_ contagem (8).
-   Dá suporte a [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s, [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s e exibições de acesso não ordenado tipado ([RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)e assim por diante).
-   As instruções atômicas estão disponíveis.
-   O suporte à precisão dupla pode estar disponível. Para obter informações sobre como determinar se a precisão dupla está disponível, consulte [**\_ \_ duplicatas de recursos do D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                              | Descrição                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novos tipos de recursos](direct3d-11-advanced-stages-cs-resources.md)<br/>      | Vários novos tipos de recursos foram adicionados no Direct3D 11.<br/>                                                                                                                                                                                                 |
| [Acessando recursos](direct3d-11-advanced-stages-cs-access.md)<br/>        | Há várias maneiras de acessar os [recursos](overviews-direct3d-11-resources-types.md).<br/>                                                                                                                                                                   |
| [Funções atômicas](direct3d-11-advanced-stages-cs-atomic-functions.md)<br/> | Para acessar um novo tipo de recurso ou memória compartilhada, use uma função intrínseca interbloqueada. As funções intercadeados têm garantia de operar atomicamente. Ou seja, é garantido que ocorram na ordem programada. Esta seção lista as funções atômicas.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Como: criar um sombreador de computação](direct3d-11-advanced-stages-compute-create.md)
</dt> </dl>

 

