---
title: Diferenças entre os efeitos 10 e os efeitos 11
description: Este tópico mostra as diferenças entre os efeitos 10 e 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641332"
---
# <a name="differences-between-effects-10-and-effects-11"></a>Diferenças entre os efeitos 10 e os efeitos 11

Este tópico mostra as diferenças entre os efeitos 10 e 11.

## <a name="device-contexts-threading-and-cloning"></a>Contextos de dispositivo, threading e clonagem

A interface ID3D10Device foi dividida em duas interfaces no Direct3D 11: ID3D11Device e ID3D11DeviceContext. Você pode criar vários ID3D11DeviceContexts para facilitar a execução simultânea em vários threads. Os efeitos 11 ampliam esse conceito para a estrutura de efeitos.

O tempo de execução dos efeitos 11 é de thread único. Por esse motivo, você não deve usar uma única instância ID3DX11Effect com vários threads simultaneamente.

Para usar o tempo de execução Effects 11 em várias instâncias, você deve criar instâncias ID3DX11Effect separadas. Como o ID3D11DeviceContext também é de thread único, você deve passar diferentes instâncias de ID3D11DeviceContext para cada instância de efeito ao aplicar. Você pode usar esses contextos de dispositivo separados para criar listas de comandos para que o thread de renderização possa aplicá-las no contexto do dispositivo imediato.

A maneira mais fácil de criar vários efeitos que encapsulam a mesma funcionalidade, para uso em vários threads, é criar um efeito e, em seguida, fazer cópias clonadas. A clonagem tem as seguintes vantagens em relação à criação de várias cópias do zero:

1.  A rotina de clonagem é mais rápida do que a rotina de criação.
2.  Os efeitos clonados compartilham sombreadores criados, blocos de estado e instâncias de classe (para que eles não precisem ser recriados).
3.  Os efeitos clonados podem compartilhar buffers constantes.
4.  Os efeitos clonados começam com o estado que corresponde ao efeito atual (valores de variável, seja ou não otimizado).

Consulte [clonar um efeito](d3d11-graphics-programming-guide-effects-cloning.md) para obter mais informações.

## <a name="effect-pools-and-groups"></a>Pools de efeitos e grupos

De longe, o uso mais predominante dos pools de efeito no Direct3D 10 era o agrupamento de materiais. Os pools de efeito foram removidos dos efeitos 11 e os grupos foram adicionados, o que é um método mais eficiente de agrupamento de materiais.

Um grupo de efeitos é simplesmente um conjunto de técnicas. Consulte [sintaxe do grupo de efeitos (Direct3D 11)](d3d11-effect-group-syntax.md) para obter mais informações.

Considere a seguinte hierarquia de efeito com quatro efeitos filho e um pool de efeito:


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



Você pode obter a mesma funcionalidade nos efeitos 11 usando grupos:


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a>Novos estágios de sombreador

Há três novos estágios de sombreador no Direct3D 11: o sombreador envoltória, o sombreador de domínio e o sombreador de computação. Os efeitos 11 lidam com isso de maneira semelhante a sombreadores de vértice, sombreadores de geometria e sombreadores de pixel.

Três novos tipos de variáveis foram adicionados aos efeitos 11:

-   HullShader
-   DomainShader
-   ComputeShader

Se você usar esses sombreadores em uma técnica, deverá rotular essa técnica como "technique11" e não "technique10". O sombreador de computação não pode ser definido na mesma passagem que qualquer outro Estado de gráfico (outros sombreadores, blocos de estado ou destinos de renderização).

## <a name="new-texture-types"></a>Novos tipos de textura

O Direct3D 11 dá suporte aos seguintes tipos de textura:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a>Exibições de acesso não ordenado

Os efeitos 11 dão suporte à obtenção e à definição dos novos tipos de exibição de acesso não ordenado. Isso funciona de maneira semelhante a texturas.

Considere estes efeitos HLSL exemplo:


```
  
RWTexture1D<float> myUAV;
```



Você pode definir essa variável em C++ da seguinte maneira:


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



O Direct3D 11 dá suporte aos seguintes tipos de exibição de acesso não ordenado:

-   RWBuffer
-   RWByteAddressBuffer
-   RWStructuredBuffer
-   RWTexture1D
-   RWTexture1DArray
-   RWTexture2D
-   RWTexture2DArray
-   RWTexture3D

## <a name="interfaces-and-class-instances"></a>Interfaces e instâncias de classe

Para a interface e a sintaxe de classe, consulte [interfaces e classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

Para usar interfaces e classes em efeitos, consulte [interfaces e classes em efeitos](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).

## <a name="addressable-stream-out"></a>Fluxo de saída endereçável

No Direct3D 10, os sombreadores de geometria podem produzir um fluxo de dados para a unidade de saída de fluxo e a unidade rasterizadora. No Direct3D11, os sombreadores de geometria podem produzir até quatro fluxos de dados para a unidade de saída do fluxo e, no máximo, um desses fluxos para a unidade do rasterizador. O **ConstructGSWithSO** intrínseco foi atualizado para refletir essa nova funcionalidade.

Consulte [sintaxe de fluxo horizontal](d3d11-graphics-reference-effect-streamout.md) para obter mais informações.

## <a name="setting-and-unsetting-device-state"></a>Definindo e desdefinindo o estado do dispositivo

Nos efeitos 10, você poderia tornar os buffers constantes e os buffers de textura gerenciados pelo usuário usando as funções [**ID3D10EffectConstantBuffer:: SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) e [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) . Depois de chamar essas funções, os efeitos 10 de tempo de execução não gerenciam mais o buffer constante ou o buffer de textura e o usuário deve preencher os dados usando a interface ID3D10Device.

Nos efeitos 11, você também pode fazer com que os blocos de estado (estado de mesclagem, estado do rasterizador, estado do estêncil de profundidade e estado de amostra) sejam gerenciados pelo usuário usando as seguintes chamadas:

-   [**ID3DX11EffectBlendVariable:: setblendstate**](id3dx11effectblendvariable-setblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable:: setamostrar**](id3dx11effectsamplervariable-setsampler.md)

Depois que você chamar essas funções, o tempo de execução dos efeitos 11 não gerenciará mais as variáveis de bloco de estado, e os valores permanecerão inalterados. Observe que, como os blocos de estado são imutáveis, o usuário deve definir um novo bloco de estado para alterar os valores.

Você também pode reverter buffers de constantes, buffers de textura e blocos de estado para o estado não gerenciado pelo usuário. Se você remover essas variáveis, o tempo de execução dos efeitos 11 continuará a ser atualizado quando necessário. Você pode usar as seguintes chamadas para remover a definição de variáveis gerenciadas pelo usuário:

-   [**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [**ID3DX11EffectBlendVariable::UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a>Afeta a máquina virtual

A máquina virtual de efeitos, que avaliou expressões complexas fora das funções, foi removida.

Não há suporte para os seguintes exemplos de expressões complexas:

1.  SetPixelShader (myPSArray (i \* 3 + j));
2.  SetPixelShader (myPSArray ((float) i);
3.  FILTER = i + 2;

Há suporte para os seguintes exemplos de expressões não complexas:

1.  SetPixelShader( myPS );
2.  SetPixelShader (myPS \[ i \] );
3.  SetPixelShader (myPS \[ uIndex \] );//uIndex é uma variável uint
4.  FILTER = i;
5.  FILTER = ANISOTROPIC;

Essas expressões podem aparecer em expressões de bloco de estado (como FILTER) e expressões Pass (como SetPixelShader).

## <a name="source-availability-and-location"></a>Disponibilidade e local de origem

Os efeitos 10 foram distribuídos em D3D10.dll. Os efeitos 11 são distribuídos como fonte, com as soluções do Visual Studio correspondentes para compilá-lo. Quando você cria aplicativos de tipo de efeitos, recomendamos que inclua a fonte de efeitos 11 diretamente nesses aplicativos.

Você pode obter efeitos 11 de [efeitos para a atualização do Direct3D 11](https://github.com/Microsoft/FX11).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 