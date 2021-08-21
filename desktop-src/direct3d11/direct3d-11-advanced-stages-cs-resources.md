---
title: Novos tipos de recursos
description: Vários novos tipos de recursos foram adicionados no Direct3D 11.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Buffer de endereço de byte (visão geral)
- Buffer de leitura/gravação (visão geral)
- Buffer estruturado (visão geral)
- Buffer de acesso não organizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ab9e6f1677770b1a40766b846f4675df9eaa3809b42838783ddb834044bfe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566296"
---
# <a name="new-resource-types"></a>Novos tipos de recursos

Vários novos tipos de recursos foram adicionados no Direct3D 11.

-   [Buffers e texturas de leitura/gravação](#readwrite-buffers-and-textures)
-   [Buffer estruturado](#structured-buffer)
-   [Buffer de endereço de byte](#byte-address-buffer)
-   [Textura ou buffer de acesso não organizado](#unordered-access-buffer-or-texture)
    -   [Anexar e consumir buffer](#append-and-consume-buffer)
-   [Tópicos relacionados](#related-topics)

## <a name="readwrite-buffers-and-textures"></a>Buffers e texturas de leitura/gravação

Os recursos do modelo de sombreador 4 são somente leitura. O modelo de sombreador 5 implementa um novo conjunto correspondente de recursos de leitura/gravação:

-   [RWBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   [RWTexture1D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d) [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)
-   [RWTexture2D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d) [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)
-   [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

Esses recursos exigem uma variável de recurso para acessar a memória (por meio da indexação), pois não há métodos para acessar a memória diretamente. Uma variável de recurso pode ser usada nos lados esquerdo e direito de uma equação; se usado no lado direito, o tipo de modelo deve ser um único componente (float, int ou uint).

## <a name="structured-buffer"></a>Buffer estruturado

Um buffer estruturado é um buffer que contém elementos de tamanhos iguais. Use uma estrutura com um ou mais tipos de membro para definir um elemento. Aqui está uma estrutura com três membros.


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



Use essa estrutura para declarar um buffer estruturado como este:


```
StructuredBuffer<MyStruct> mySB;
```



Além da indexação, um buffer estruturado dá suporte ao acesso a um único membro como este:


```
float4 myColor = mySb[27].Color;
```



Use os seguintes tipos de objeto para acessar um buffer estruturado:

-   [StructuredBuffer é](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) um buffer estruturado somente leitura.
-   [RWStructuredBuffer é](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) um buffer estruturado de leitura/gravação.

[Funções atômicas](direct3d-11-advanced-stages-cs-atomic-functions.md) que implementam operações interlocked são permitidas em elementos int e uint em **um RWStructuredBuffer.**

## <a name="byte-address-buffer"></a>Buffer de endereço de byte

Um buffer de endereço de byte é um buffer cujo conteúdo pode ser endereço por um deslocamento de byte. Normalmente, o conteúdo de um [buffer](overviews-direct3d-11-resources-buffers-intro.md) é indexado por elemento usando um stride para cada elemento (S) e o número do elemento (N), conforme determinado por S \* N. Um buffer de endereço de byte, que também pode ser chamado de buffer bruto, usa um deslocamento de valor de byte do início do buffer para acessar dados. O valor de byte deve ser um múltiplo de quatro para que seja alinhado a DWORD. Se qualquer outro valor for fornecido, o comportamento será indefinido.

O modelo de sombreador 5 introduz objetos para acessar um buffer de endereço de [byte](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) somente leitura, bem como um buffer de endereço de [byte de leitura/gravação.](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) O conteúdo de um buffer de endereço de byte foi projetado para ser um inteiro sem sinal de 32 bits; se o valor no buffer não for realmente um inteiro sem sinal, use uma função como [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) para lê-lo.

## <a name="unordered-access-buffer-or-texture"></a>Textura ou buffer de acesso não organizado

Um recurso de acesso não organizado (que inclui buffers, texturas e matrizes de textura – sem multisampling), permite acesso de leitura/gravação não organizado temporalmente de vários threads. Isso significa que esse tipo de recurso pode ser lido/gravado simultaneamente por vários threads sem gerar conflitos de memória por meio do uso de [Funções Atômicas](direct3d-11-advanced-stages-cs-atomic-functions.md).

Crie um buffer ou textura de acesso não organizado chamando uma função como [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) ou [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e passando o sinalizador **D3D11 \_ BIND \_ UNORDERED \_ ACCESS** da enumeração DO SINALIZADOR [**BIND D3D11. \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)

Os recursos de acesso não organizado só podem ser vinculados a sombreadores de pixel e sombreadores de computação. Durante a execução, sombreadores de pixel ou sombreadores de computação em execução em paralelo têm os mesmos recursos de acesso não organizados vinculados.

### <a name="append-and-consume-buffer"></a>Anexar e consumir buffer

Um buffer de acréscimo e consumo é um tipo especial de um recurso não pedido que dá suporte à adição e remoção de valores do final de um buffer semelhante à maneira como uma pilha funciona.

Um buffer de anexação e consumo deve ser um buffer estruturado:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

Use esses recursos por meio de seus métodos, esses recursos não usam variáveis de recurso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do sombreador de computação](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 