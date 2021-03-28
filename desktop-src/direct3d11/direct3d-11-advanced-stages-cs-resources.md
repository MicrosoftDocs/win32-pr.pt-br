---
title: Novos tipos de recursos
description: Vários novos tipos de recursos foram adicionados no Direct3D 11.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Buffer de endereço de byte (visão geral)
- Buffer de leitura/gravação (visão geral)
- Buffer estruturado (visão geral)
- Buffer de acesso não ordenado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366349"
---
# <a name="new-resource-types"></a>Novos tipos de recursos

Vários novos tipos de recursos foram adicionados no Direct3D 11.

-   [Buffers de leitura/gravação e texturas](#readwrite-buffers-and-textures)
-   [Buffer estruturado](#structured-buffer)
-   [Buffer de endereço de byte](#byte-address-buffer)
-   [Buffer ou textura de acesso não ordenado](#unordered-access-buffer-or-texture)
    -   [Acrescentar e consumir buffer](#append-and-consume-buffer)
-   [Tópicos relacionados](#related-topics)

## <a name="readwrite-buffers-and-textures"></a>Buffers de leitura/gravação e texturas

Os recursos do Shader Model 4 são somente leitura. O Shader Model 5 implementa um novo conjunto correspondente de recursos de leitura/gravação:

-   [RWBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   [RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)
-   [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)
-   [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

Esses recursos exigem uma variável de recurso para acessar a memória (por meio de indexação), pois não há métodos para acessar a memória diretamente. Uma variável de recurso pode ser usada nos lados esquerdo e direito de uma equação; Se usado no lado direito, o tipo de modelo deve ser um componente único (float, int ou uint).

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



Use esta estrutura para declarar um buffer estruturado como este:


```
StructuredBuffer<MyStruct> mySB;
```



Além da indexação, um buffer estruturado dá suporte ao acesso a um único membro como este:


```
float4 myColor = mySb[27].Color;
```



Use os seguintes tipos de objeto para acessar um buffer estruturado:

-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) é um buffer estruturado somente leitura.
-   [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) é um buffer estruturado de leitura/gravação.

[Funções atômicas](direct3d-11-advanced-stages-cs-atomic-functions.md) que implementam operações interbloqueadas são permitidas em elementos int e uint em um **RWStructuredBuffer**.

## <a name="byte-address-buffer"></a>Buffer de endereço de byte

Um buffer de endereço de byte é um buffer cujo conteúdo é endereçável por um deslocamento de byte. Normalmente, o conteúdo de um [buffer](overviews-direct3d-11-resources-buffers-intro.md) é indexado por elemento usando um stride para cada elemento e o número do elemento (N), conforme fornecido por S \* N. Um buffer de endereço de byte, que também pode ser chamado de buffer bruto, usa um deslocamento de valor de byte do início do buffer para acessar dados. O valor de byte deve ser um múltiplo de quatro para que seja alinhado em DWORD. Se qualquer outro valor for fornecido, o comportamento será indefinido.

O modelo de sombreador 5 apresenta objetos para acessar um [buffer de endereço de byte somente leitura](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) , bem como um [buffer de endereço de byte de leitura/gravação](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer). O conteúdo de um buffer de endereço de byte é projetado para ser um inteiro sem sinal de 32 bits; Se o valor no buffer não for realmente um inteiro sem sinal, use uma função como [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) para lê-lo.

## <a name="unordered-access-buffer-or-texture"></a>Buffer ou textura de acesso não ordenado

Um recurso de acesso não ordenado (que inclui buffers, texturas e matrizes de textura-sem várias amostras) permite o acesso de leitura/gravação não ordenado de forma temporal de vários threads. Isso significa que esse tipo de recurso pode ser lido/gravado simultaneamente por vários threads sem gerar conflitos de memória por meio do uso de [funções atômicas](direct3d-11-advanced-stages-cs-atomic-functions.md).

Crie uma textura ou um buffer de acesso não ordenado chamando uma função como [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) ou [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e passando o sinalizador de **\_ \_ \_ acesso de vínculo não ordenado de D3D11** da enumeração de [**\_ \_ sinalizador de associação D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .

Os recursos de acesso não ordenados só podem ser associados a sombreadores de pixel e sombreadores de computação. Durante a execução, sombreadores de pixel ou sombreadores de computação executados em paralelo têm os mesmos recursos de acesso não ordenados associados.

### <a name="append-and-consume-buffer"></a>Acrescentar e consumir buffer

Um buffer de acréscimo e consumo é um tipo especial de recurso não ordenado que dá suporte à adição e à remoção de valores do final de um buffer semelhante ao modo como uma pilha funciona.

Um buffer de acréscimo e consumo deve ser um buffer estruturado:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

Use esses recursos por meio de seus métodos, esses recursos não usam variáveis de recurso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do sombreador de computação](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 