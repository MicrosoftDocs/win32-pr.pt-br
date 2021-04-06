---
description: A neblina de pixels obtém seu nome do fato de que ele é calculado por pixel no driver do dispositivo.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Sombra de pixel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825489"
---
# <a name="pixel-fog-direct3d-9"></a>Sombra de pixel (Direct3D 9)

A neblina de pixels obtém seu nome do fato de que ele é calculado por pixel no driver do dispositivo. Isso é diferente da sombra do vértice, que é computada pelo pipeline durante os cálculos de transformação e iluminação. A neblina de pixel às vezes é chamada de neblina de tabela porque alguns drivers usam uma tabela de pesquisa precalculada para determinar o fator de neblina, usando a profundidade de cada pixel a ser aplicada em cálculos de mesclagem. Ele pode ser aplicado usando qualquer fórmula de neblina identificada por membros do tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) . As implementações dessas fórmulas são específicas do driver. Se um driver não oferecer suporte a uma fórmula de neblina complexa, ele deverá degradar uma fórmula menos complexa.

## <a name="eye-relative-vs-z-based-depth"></a>Eye-Relative vs. profundidade baseada em Z

Para aliviar os artefatos gráficos relacionados à neblina causados por distribuição desigual de valores z em um buffer de profundidade, a maioria dos dispositivos de hardware usa profundidade relativa aos olhos em vez de valores de profundidade baseados em z para sombra de pixel. A profundidade relativa aos olhos é essencialmente o elemento w de um conjunto de coordenadas homogêneos. O Microsoft Direct3D usa o recíproco do elemento RHW de uma coordenada de espaço de dispositivo definida para reproduzir o verdadeiro. Se um dispositivo oferecer suporte à neblina de olho, ele definirá o sinalizador **D3DPRASTERCAPS \_ WFOG** no membro RasterCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) quando você chamar o método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) . Com exceção do rasterizador de referência, os dispositivos de software sempre usam z para calcular os efeitos de neblina de pixel.

Quando a neblina relativa a olho é suportada, o sistema usa automaticamente a profundidade relativa ao olho em vez da profundidade baseada em z se a matriz de projeção fornecida produza valores z no espaço de mundo equivalente aos valores w no espaço do dispositivo. Você define a matriz de projeção chamando o método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) , usando o \_ valor de projeção D3DTS e passando uma estrutura [**D3DMATRIX**](d3dmatrix.md) que representa a matriz desejada. Se a matriz de projeção não estiver em conformidade com esse requisito, os efeitos de neblina não serão aplicados corretamente. Para obter detalhes sobre como produzir uma matriz compatível, consulte [transformação de projeção (Direct3D 9)](projection-transform.md).

Direct3D usa matriz de projeção atual definida em seus cálculos de profundidade com base em w. Como resultado, um aplicativo deve definir uma matriz de projeção compatível para receber os recursos baseados em w, mesmo que não use o pipeline de transformação do Direct3D.

O Direct3D verifica a quarta coluna da matriz de projeção. Se os coeficientes forem \[ 0, 0, 0, 1 \] (para uma projeção afim), o sistema usará valores de profundidade baseados em z para neblina. Nesse caso, você também deve especificar as distâncias inicial e final para efeitos de neblina linear no espaço do dispositivo, que varia de 0,0 no ponto mais próximo para o usuário e 1,0 no ponto mais distante.

## <a name="using-pixel-fog"></a>Usando a neblina de pixel

Use as etapas a seguir para habilitar a neblina de pixel em seu aplicativo.

1.  Habilite a mesclagem de neblina definindo o \_ estado de RENDERIZAÇÃO D3DRS FOGENABLE como **true**.
2.  Defina a cor de neblina desejada no \_ estado de RENDERIZAÇÃO D3DRS FOGCOLOR.
3.  Escolha a fórmula de neblina a ser usada definindo o \_ estado de RENDERIZAÇÃO D3DRS FOGTABLEMODE para o membro correspondente do tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .
4.  Defina os parâmetros de neblina conforme desejado para o modo de neblina selecionado nos Estados de renderização associados. Isso inclui as distâncias inicial e final para a neblina linear e densidade de neblina para o modo de neblina exponencial.

O exemplo a seguir mostra o que essas etapas podem parecer no código.


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



Alguns parâmetros de neblina são necessários como valores de ponto flutuante, mesmo que o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceite somente valores DWORD no segundo parâmetro. O exemplo anterior fornece os valores de ponto flutuante para **IDirect3DDevice9:: Setrenderingstate** sem conversão de dados, convertendo os endereços das variáveis de ponto flutuante como ponteiros DWORD e, em seguida, desfazendo a referência a eles.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de neblina](fog-types.md)
</dt> </dl>

 

 
