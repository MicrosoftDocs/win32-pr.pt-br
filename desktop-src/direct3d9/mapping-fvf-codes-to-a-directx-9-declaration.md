---
description: Esta tabela mapeia códigos FVF para uma estrutura D3DVERTEXELEMENT9.
ms.assetid: de865481-2a08-4d25-967c-8e68b7affe8d
title: Mapeando códigos FVF para uma declaração direct3D 9 (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8ef4d5e8e29c4c7f6af8d82b650b4898c57d900b92b8dd45ca2368bb9eacce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799072"
---
# <a name="mapping-fvf-codes-to-a-direct3d-9-declaration-direct3d-9"></a>Mapeando códigos FVF para uma declaração direct3D 9 (Direct3D 9)

Esta tabela mapeia códigos FVF para uma [**estrutura D3DVERTEXELEMENT9.**](d3dvertexelement9.md)



| Fvf                                                   | Tipo de dados                                                           | Uso                                                                         | Índice de uso |
|-------------------------------------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------|-------------|
| D3DFVF \_ XYZ                                           | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE \_ POSITION                                                        | 0           |
| D3DFVF \_ XYZRHW                                        | D3DDECLTYPE \_ FLOAT4                                                 | D3DDECLUSAGE \_ POSITIONT                                                       | 0           |
| D3DFVF \_ XYZW                                          | D3DDECLTYPE \_ FLOAT4                                                 | D3DDECLUSAGE \_ POSITION                                                        | 0           |
| D3DFVF \_ XYZB5 e D3DFVF \_ LASTBETA \_ UBYTE4            | D3DVSDT \_ FLOAT3, D3DVSDT \_ FLOAT4, D3DVSDT \_ UBYTE4                   | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5 e D3DFVF \_ LASTBETA \_ D3DCOLOR          | D3DVSDT \_ FLOAT3, D3DVSDT \_ FLOAT4, D3DVSDT \_ D3DCOLOR                 | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5                                         | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT4, D3DDECLTYPE \_ FLOAT1       | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n=1..4)                                | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOATn                            | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT                             | 0           |
| D3DFVF \_ XYZBn (n=1..4) e D3DFVF \_ LASTBETA \_ UBYTE4   | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT(n-1), D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n=1..4) e D3DFVF \_ LASTBETA \_ D3DCOLOR | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT(n-1), D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ NORMAL                                        | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE \_ NORMAL                                                          | 0           |
| D3DFVF \_ PSIZE                                         | D3DDECLTYPE \_ FLOAT1                                                 | D3DDECLUSAGE \_ PSIZE                                                           | 0           |
| D3DFVF \_ DIFUSO                                       | D3DDECLTYPE \_ D3DCOLOR                                               | COR D3DDECLUSAGE \_                                                           | 0           |
| D3DFVF \_ SPECULAR                                      | D3DDECLTYPE \_ D3DCOLOR                                               | COR D3DDECLUSAGE \_                                                           | 1           |
| D3DFVF \_ TEXCOORDSIZEm(n)                              | D3DDECLTYPE \_ FLOATm                                                 | D3DDECLUSAGE \_ TEXCOORD                                                        | n           |



 

## <a name="vertex-declarations-with-d3ddeclusage_positiont"></a>Declarações de vértice com D3DDECLUSAGE \_ POSITIONT

A presença de um elemento de vértice com (D3DUSAGE POSITIONT, 0) é usada para indicar ao dispositivo que os dados de vértice que estão chegando já passaram pelo processamento de vértice (como um FVF com conjunto de bits \_ \_ XYZRHW D3DFVF). Em tempo de desenho, se a declaração atualmente definida tiver um elemento com a semântica (D3DUSAGE POSITIONT, 0), todo o processamento de vértice será ignorado (assim como se um FVF com o \_ bit XYZRHW D3DFVF tivesse \_ sido definido).

Há algumas restrições em declarações de vértice com (D3DDECLUSAGE \_ POSITIONT, 0):

-   Somente o fluxo zero pode ser usado em tais declarações.
-   Os elementos de vértice devem ser classificação aumentando o deslocamento de fluxo.
-   O deslocamento de fluxo deve ser alinhado com DWORD.
-   O mesmo par (Uso, Índice de Uso) deve ser listado apenas uma vez.
-   Somente o método D3DDECLMETHOD \_ DEFAULT pode ser usado.
-   Outros elementos de vértice não podem ter a semântica (D3DDECLUSAGE \_ POSITION, 0).

Além disso, há algumas restrições sobre essa declaração relacionada à versão do driver de dispositivo. Essas restrições estão em vigor porque o Direct3D envia essas declarações diretamente para o driver sem fazer nenhuma conversão.

## <a name="vertex-declarations-without-d3ddeclusage_positiont"></a>Declarações de vértice sem D3DDECLUSAGE \_ POSITIONT

O runtime valida a criação de declarações. A seguir estão as regras gerais para quais declarações são legais.

-   Todos os elementos de vértice de um fluxo devem ser consecutivos e classificar por deslocamento.
-   O deslocamento de fluxo deve ser alinhado com DWORD.
-   O mesmo par (Uso, Índice de Uso) deve ser listado apenas uma vez.
-   Se D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET estiver definido,
    -   Vários elementos de vértice podem compartilhar o mesmo deslocamento em um fluxo.
    -   Os elementos de vértice podem ser de tipos diferentes que podem ser de tamanhos diferentes.
    -   Os elementos de vértice podem se sobrepor arbitrariamente. Por exemplo, um elemento pode começar em um local de um fluxo que está, ao mesmo tempo, no meio de outro elemento.
    -   Os elementos de vértice têm permissão para ter deslocamento de fluxo em qualquer ordem.
-   O número de elementos de vértice não pode ser maior que 64.
-   UsageIndex deve estar no intervalo \[ de 0 a 15 \] .
-   A declaração, usada com a API DrawPrimitive, não deve ter elementos de vértice diferentes de D3DDECLMETHOD \_ DEFAULT, D3DDECLMETHOD \_ LOOKUPPRESAMPLED ou D3DDECLMETHOD \_ LOOKUP.
-   A declaração , que contém D3DDECLMETHOD LOOKUP ou LOOKUPPRESAMPLED, deve ser usada somente com o \_ pipeline de vértice programável.
-   A declaração, usada com a API DrawRectPatch/DrawTriPatch, não pode ter elementos de vértice com D3DDECLMETHOD \_ LOOKUPPRESAMPLED ou D3DDECLMETHOD \_ LOOKUP.
-   A declaração deve ter apenas um elemento com o método D3DDECLMETHOD LOOKUP ou \_ D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   A declaração com D3DDECLMETHOD LOOKUP ou \_ D3DDECLMETHOD LOOKUPPRESAMPLED não deve ter elementos diferentes de \_ D3DDECLMETHOD DEFAULT, pois o mapeamento de deslocamento é feito somente para \_ N patches.
-   Elementos de vértice com D3DDECLMETHOD LOOKUP ou D3DDECLMETHOD LOOKUPPRESAMPLED só podem ser usados com a semântica \_ \_ (D3DDECLUSAGE \_ SAMPLE, n) e vice-versa.
-   Se um elemento de vértice com o método D3DDECLMETHOD LOOKUP tiver um índice de fluxo e deslocamento de um elemento de vértice já existente, esse elemento de vértice deverá ter o mesmo tipo de \_ dados.
-   Um elemento de vértice com o método D3DDECLMETHOD LOOKUP deve ter o tipo de dados \_ D3DDECLTYPE \_ FLOAT2/3/4
-   Elementos de vértice com os tipos D3DDECLMETHOD \_ CROSSUV, D3DDECLMETHOD PARTIALU e \_ D3DDECLMETHOD PARTIALV devem ter um deslocamento de um elemento de vértice com um tipo de dados \_ compatível.
-   Um elemento de vértice com o método D3DDECLMETHOD UV ou \_ D3DDECLMETHOD LOOKUPPRESAMPLED deve ter o tipo \_ D3DDECLTYPE UNUSED, o índice de fluxo zero e o deslocamento de fluxo \_ zero.
-   Declarações com métodos D3DDECLMETHOD \_ UV, D3DDECLMETHOD \_ partiald e D3DDECLMETHOD \_ PARTIALV só podem ser usadas com DrawRectPatch.
-   O uso \_ de D3DDECLUSAGE TESSFACTOR deve ser usado somente com o tipo de dados D3DDECLTYPE \_ FLOAT1 e o índice de uso 0.
-   Quando uma declaração é usada para mosaico (DrawRectPatch, DrawTriPatch, N-patches), o tipo de dados deve ser menor ou igual a D3DDECLTYPE \_ SHORT4.
-   As declarações que contêm métodos que exigem determinados recursos de dispositivo (por exemplo, mapeamento de deslocamento, RT-patches) só poderão ser criadas se o dispositivo oferecer suporte a eles.
-   Uma declaração de vértice usada para desenhar pontos e linhas não pode ter métodos diferentes de D3DDECLMETHOD \_ padrão.
-   As declarações que podem ser criadas também dependem dos recursos do driver.

## <a name="driver-considerations"></a>Considerações sobre o driver

### <a name="pre-direct3d-9-drivers"></a>Drivers anteriores ao Direct3D 9

-   A declaração de entrada deve ser traduzível para um FVF válido (ter a mesma ordem de elementos de vértice e seus tipos de dados).
-   As lacunas nas coordenadas de textura não são permitidas. Isso significa que, se houver um elemento de vértice com (D3DDECLUSAGE \_ TEXCOORD, n), também deverá haver um elemento Vertex com (D3DDECLUSAGE \_ TEXCOORD, n-1).

### <a name="direct3d-9-drivers-without-pixel-shader-version-3-support"></a>Drivers do Direct3D 9 sem suporte para o pixel shader versão 3

-   A declaração de entrada deve ser traduzível para um FVF válido (ter a mesma ordem de elementos de vértice e seus tipos de dados).
-   As lacunas nas coordenadas de textura são permitidas.

### <a name="direct3d-9-drivers-with-pixel-shader-version-3-support"></a>Drivers do Direct3D 9 com suporte para o pixel shader versão 3

Declarações mais gerais são permitidas.

-   Elementos de vértice podem estar em ordem arbitrária e podem ter qualquer tipo de dados.
-   Vários elementos de vértice podem compartilhar o mesmo deslocamento de fluxo e ser de um tipo diferente ao mesmo tempo se D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET for definido pelo dispositivo.

## <a name="vertex-declaration-usage-with-the-programmable-vertex-pipeline"></a>Uso de declaração de vértice com o pipeline de vértice programável

-   No momento do desenho, o Direct3D procura a mesma combinação de "índice de uso de uso" na declaração de vértice atual e a função de sombreador de vértice atual. Quando a combinação é encontrada, o registro da função de sombreador DCL é usado como o destino para o elemento Vertex.
-   Quando um elemento Vertex na declaração de vértice atual tem um uso que não é encontrado no sombreador de vértice atual, esse elemento vertex é ignorado.
-   Ao usar uma versão de sombreadores de vértice inferior a 2,0, toda a semântica mencionada no código do sombreador precisa estar presente na declaração associada no tempo de desenho. Ao usar os sombreadores de vértice 2,0 e acima, essa restrição que permite que os aplicativos usem declarações de vértice diferentes com o mesmo sombreador de vértices não existe. Isso é útil quando um sombreador de vértice lê dados de entrada com base em condições estáticas. Os registros de sombreador de vértice não inicializados porque isso terá valores indefinidos.

Há restrições adicionais ao usar com o processamento de vértice de hardware em um driver DirectX 8:

-   Os elementos de vértice não podem se sobrepor nem compartilhar o mesmo deslocamento.
-   Os tipos de dados são limitados ao que o driver DirectX 8 pode entender.

O CreateVertexDeclaration poderá falhar se a declaração fornecida não puder ser convertida em uma declaração de estilo DirectX 8. Para um dispositivo de modo misto, essa falha ocorrerá no \* momento do empate porque esse é o único momento em que ele pode ser conhecido se esse sombreador está sendo usado com o processamento de vértice de hardware ou software.

## <a name="vertex-declaration-usage-with-the-fixed-function-pipeline"></a>Uso de declaração de vértice com o pipeline de função fixa

Somente declarações que aderem às seguintes regras podem ser usadas:

-   Não deve haver nenhuma lacuna entre os elementos de vértice (SKIP não é permitido em uma declaração DirectX 8, que é usada para o pipeline de função fixo).
-   Semântica (D3DDECLUSAGE \_ posição, 0) deve ser especificada e deve ter o \_ tipo de dados D3DDECLTYPE FLOAT3.
-   Um elemento Vertex com o método D3DDECLMETHOD \_ UV deve especificar uso D3DDECLUSAGE \_ TEXCOORD ou D3DDECLUSAGE \_ BLENDWEIGHT.
-   Um elemento Vertex com o método D3DDECLMETHOD \_ partialu, \_ PARTIALV ou \_ CROSSUV só pode ser usado com D3DDECLUSAGE \_ Position, \_ normal, \_ BLENDWEIGHT ou \_ TEXCOORD e deve usar o tipo de entrada D3DDECLTYPE \_ FLOAT3.

Quando uma declaração é usada com o processamento de vértice de hardware em um driver DirectX 8, o tempo de execução do Direct3D converte-o em uma declaração de estilo DirectX 8 com as seguintes regras:

-   Os elementos de vértice não podem compartilhar o mesmo deslocamento em um fluxo e não podem se sobrepor.
-   O tipo de dados deve ser menor ou igual a D3DDECLTYPE \_ SHORT4.
-   Somente os métodos a seguir são permitidos: D3DDECLMETHOD \_ Default, D3DDECLMETHOD \_ CROSSUV e D3DDECLMETHOD \_ UV
-   O [mapeamento entre uma declaração do Direct3D 9 e uma declaração do Direct3D 8 (Direct3D 9)](mapping-between-a-directx-9-declaration-and-directx-8.md) mostra quais semânticas do Direct3D 9 podem ser convertidas para a declaração do estilo DirectX 8. Uso e UsageIndex são convertidos em um valor de registro.
-   Se houver n elementos Vertex em uma declaração e 0-m (m < n) for mapeado para um FVF (elementos descritos no [mapeamento entre uma declaração Direct3D e códigos FVF (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md)), mas m + 1 não, então:
    -   Se um dos m + 2 até os elementos de vértice n-1 mapearem para FVF/dx8decl, a declaração será inválida.
    -   Os elementos de 0 a m são convertidos (pelo tempo de execução para DirectX 8 e drivers mais antigos, e pelos drivers do Direct3D 9) usando o [mapeamento entre uma declaração de Direct3D e códigos de FVF (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md), m + 1, m + 2 até que n-1 seja mapeado para texcoord contíguos (k), texcoord (k + 1), a partir de qualquer texcoord
    -   O tipo de dados em um texcoord mapeado é considerado como float \[ 1234 \] substituindo qualquer tipo de dados que o elemento atual contém (mas o mesmo tamanho). Portanto, o tipo de dados existente pode ser algo que não está no [mapeamento entre uma declaração de Direct3D e códigos de FVF (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md).
    -   Se k atingir 8, a declaração será inválida para FVF/dx8decl.
    -   Se algum mapeamento para texcoords tiver ocorrido, toda a declaração será necessária para não ter nenhum elemento com método de geração diferente de padrão ou a declaração será inválida para FVF/dx8decl.

## <a name="using-vertex-declarations-with-processvertices"></a>Usando declarações de vértice com ProcessVertices

Uma declaração de vértice pode ser usada para descrever a saída de ProcessVertices. Essa declaração deve aderir às seguintes regras:

-   Somente o fluxo 0 deve ser usado.
-   Somente \_ métodos padrão D3DDECLMETHOD são permitidos.
-   Somente \_ os tipos de dados D3DDECLTYPE floatn ou D3DDECLTYPE \_ D3DCOLOR podem ser usados.
-   Os elementos de vértice não podem compartilhar o mesmo deslocamento ou se sobrepõem.
-   Elementos de vértice com ( \_ posição D3DDECLUSAGE, 0) ou (D3DDECLUSAGE de \_ posição, 0) não são necessários.
-   Elementos de vértice com ( \_ posição D3DDECLUSAGE, 0) e (D3DDECLUSAGE \_ posição, 0) não podem estar presentes na mesma declaração.
-   O sombreador atual do vértice deve ser a versão 3,0 ou superior quando tal declaração for usada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declaração de vértice](vertex-declaration.md)
</dt> </dl>

 

 



