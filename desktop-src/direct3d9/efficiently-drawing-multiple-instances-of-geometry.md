---
description: Considerando uma cena que contém muitos objetos que usam a mesma geometria, você pode desenhar muitas instâncias dessa geometria em diferentes orientações, tamanhos, cores e assim por diante com um desempenho drasticamente melhor, reduzindo a quantidade de dados que você precisa fornecer ao renderador.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Desenho eficiente de várias instâncias de geometria (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70586142b58076e5010083f61aeff360aa245a298e5d010fb487aed8b5843ec8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122356"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a>Desenho eficiente de várias instâncias de geometria (Direct3D 9)

Considerando uma cena que contém muitos objetos que usam a mesma geometria, você pode desenhar muitas instâncias dessa geometria em diferentes orientações, tamanhos, cores e assim por diante com um desempenho drasticamente melhor, reduzindo a quantidade de dados que você precisa fornecer ao renderador.

Isso pode ser feito por meio do uso de duas técnicas: a primeira para desenhar geometria indexada e a segunda para geometria não indexada. Ambas as técnicas usam dois buffers de vértice: um para fornecer dados de geometria e outro para fornecer dados de instância por objeto. Os dados da instância podem ser uma ampla variedade de informações, como transformação, dados de cores ou dados de iluminação, basicamente qualquer coisa que você possa descrever em uma declaração de vértice. Desenhar muitas instâncias de geometria com essas técnicas pode reduzir drasticamente a quantidade de dados enviados ao renderista.

-   [Desenhando geometria indexada](#drawing-indexed-geometry)
    -   [Comparação de desempenho de geometria indexada](#indexed-geometry-performance-comparison)
-   [Desenhando geometria não indexada](#drawing-non-indexed-geometry)
    -   [Comparação de desempenho de geometria não indexada](#non-indexed-geometry-performance-comparison)
-   [Tópicos relacionados](#related-topics)

## <a name="drawing-indexed-geometry"></a>Desenhando geometria indexada

O buffer de vértice contém dados por vértice definidos por uma declaração de vértice. Suponha que parte de cada vértice contenha dados geometry e parte de cada vértice contenha dados de instância por objeto, conforme mostrado no diagrama a seguir.

![diagrama de um buffer de vértice para geometria indexada](images/drawingmultipleinstances.png)

Essa técnica requer um dispositivo que dá suporte ao modelo de sombreador \_ de vértice 30. Essa técnica funciona com qualquer sombreador programável, mas não com o pipeline de funções fixas.

Para os buffers de vértice mostrados acima, aqui estão as declarações de buffer de vértice correspondentes:


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Essas declarações definem dois buffers de vértice. A primeira declaração (para o fluxo 0, indicado pelos zeros na coluna 1) define os dados de geometria que consistem em: posição, normal, tangente, binormal e dados de coordenada de textura.

A segunda declaração (para o fluxo 1, indicado pelos da coluna 1) define os dados da instância por objeto. Cada instância é definida por quatro números de ponto flutuante de quatro componentes e uma cor de quatro componentes. Os primeiros quatro valores podem ser usados para inicializar uma matriz 4x4, o que significa que esses dados serão exclusivamente tamanho, posição e rotação de cada instância da geometria. Os quatro primeiros componentes usam uma semântica de coordenada de textura que, nesse caso, significa "esse é um número geral de quatro componentes". Quando você usa dados arbitrários em uma declaração de vértice, use uma semântica de coordenada de textura para marcá-los. O último elemento no fluxo é usado para dados de cores. Isso pode ser aplicado no sombreador de vértice para dar a cada instância uma cor exclusiva.

Antes de renderizar, você precisa chamar [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) para vincular os fluxos de buffer de vértice ao dispositivo. Aqui está um exemplo que vincula os dois buffers de vértice:


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) usa [D3DSTREAMSOURCE \_ INDEXEDDATA](other-direct3d-constants.md) para identificar os dados de geometria indexados. Nesse caso, o fluxo 0 contém os dados indexados que descrevem a geometria do objeto. Esse valor é logicamente combinado com o número de instâncias da geometria a ser desenhada.

Observe que D3DSTREAMSOURCE INDEXEDDATA e o número de instâncias a serem desenhadas sempre devem \_ ser definidos no fluxo zero.

Na segunda chamada, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) usa [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) para identificar o fluxo que contém os dados da instância. Esse valor é combinado logicamente com 1, pois cada vértice contém um conjunto de dados de instância.

As duas últimas chamadas para [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) vinculam os ponteiros de buffer de vértice ao dispositivo.

Quando terminar de renderizar os dados da instância, redefina a frequência de fluxo de vértice de volta para seu estado padrão (que não usa instanciação). Como este exemplo usou dois fluxos, de definido ambos os fluxos, conforme mostrado abaixo:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a>Comparação de desempenho de geometria indexada

Embora não seja possível chegar a uma única conclusão sobre o quanto essa técnica pode reduzir o tempo de renderização em cada aplicativo, considere a diferença na quantidade de dados transmitidos para o runtime e no número de alterações de estado que serão reduzidas se você usar a técnica de instanciamento. Essa sequência de renderização aproveita o desenho de várias instâncias da mesma geometria:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Observe que o loop de renderização é chamado uma vez, os dados geometry são transmitidos uma vez e n instâncias são transmitidas uma vez. Esta próxima sequência de renderização é idêntica na funcionalidade, mas não aproveita a instanciamento:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



Observe que todo o loop de renderização é envolvido por um segundo loop para desenhar cada objeto. Agora os dados de geometria são transmitidos para o renderador n vezes (em vez de uma vez) e os estados de pipeline também podem ser definidos com redundância para cada objeto desenhado. É muito provável que essa sequência de renderização seja significativamente mais lenta. Observe também que os parâmetros para [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) não foram alterados entre os dois loops de renderização.

## <a name="drawing-non-indexed-geometry"></a>Desenhando geometria não indexada

Em [Geometria Indexada de Desenho,](#drawing-indexed-geometry)os buffers de vértice foram configurados para desenhar várias instâncias de geometria indexada com maior eficiência. Você também pode usar [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) para desenhar geometria não indexada. Isso requer um layout de buffer de vértice diferente e tem restrições diferentes. Para desenhar geometria não indexada, prepare seus buffers de vértice como o diagrama a seguir.

![diagrama de um buffer de vértice para geometria não indexada](images/olderstyleinstancing.png)

Essa técnica não é suportada pela aceleração de hardware em nenhum dispositivo. Ele só tem suporte no processamento de vértice de software e funcionará apenas com [ \_ sombreadores \_ vs. 3 0.](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md)

Como essa técnica funciona com geometria não indexada, não há nenhum buffer de índice. Como mostra o diagrama, o buffer de vértice que contém geometria contém n cópias dos dados de geometria. Para cada instância desenhada, os dados de geometria são lidos do primeiro buffer de vértice e os dados da instância são lidos do segundo buffer de vértice.

Aqui estão as declarações de buffer de vértice correspondentes:


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Essas declarações são idênticas às declarações feitas no exemplo de geometria indexada. Mais uma vez, a primeira declaração (para o fluxo 0) define os dados de geometria e a segunda declaração (para o fluxo 1) define os dados da instância por objeto. Ao criar o primeiro buffer de vértice, carregue-o com o número de instâncias dos dados de geometria que você desenhará.

Antes de renderizar, você precisa configurar o divisor que informa ao runtime como dividir o primeiro buffer de vértice em n instâncias. Em seguida, de definir o [**divisor usando SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) desta forma:


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



A primeira chamada para [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) diz que o fluxo 0 contém n instâncias de vértices m. [**Em seguida, SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) vincula o fluxo 0 ao buffer de vértice geometry.

Na segunda chamada, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifica o fluxo 1 como a origem dos dados da instância. O segundo parâmetro é o número de vértices em cada objeto (m). Lembre-se de que o fluxo de dados da instância sempre deve ser declarado como o segundo fluxo. [**Em seguida, SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) vincula o fluxo 1 ao buffer de vértice que contém os dados da instância.

Quando terminar de renderizar os dados da instância, redefina a frequência de fluxo de vértice de volta para seu estado padrão. Como este exemplo usou dois fluxos, de definido ambos os fluxos, conforme mostrado abaixo:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a>Comparação de desempenho de geometria não indexada

A principal vantagem desse estilo de instanciamento é que ele pode ser usado em geometria não indexada. Embora não seja possível chegar a uma única conclusão sobre o quanto essa técnica pode reduzir o tempo de renderização em cada aplicativo, considere a diferença na quantidade de dados transmitidos para o runtime e o número de alterações de estado que serão reduzidas para a seguinte sequência de renderização:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Observe que o loop de renderização é chamado uma vez. Os dados de geometria são transmitidos uma vez, embora haja n instâncias da geometria sendo transmitida. Os dados do buffer de vértice da instância são transmitidos uma vez. Esta próxima sequência de renderização é idêntica na funcionalidade, mas não aproveita a instanciamento:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



Sem instanciá-lo, o loop de renderização precisa ser envolvido por um segundo loop para desenhar cada objeto. Ao eliminar o segundo loop de renderização, você deve esperar um melhor desempenho devido a menos alterações de estado de renderização chamadas dentro do loop.

Em geral, é razoável esperar que a técnica indexada ( Geometria[Indexada](#drawing-indexed-geometry)de Desenho ) seja melhor do que a técnica não indexada[(](#drawing-non-indexed-geometry)Desenhando geometria não indexada ) porque a técnica indexada transmite apenas uma cópia dos dados de geometria. Observe que os parâmetros para [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) não foram alterados para nenhuma das sequências de renderização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos avançados](advanced-topics.md)
</dt> <dt>

[Exemplo de instanciamento](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)
</dt> </dl>

 

 
