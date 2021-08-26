---
description: Quando o sistema executa o vértice fogging, ele aplica cálculos de neblina em cada vértice em um polígono e, em seguida, interpola os resultados em toda a face do polígono durante a rasterização.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Neblina de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76196ba0489ac58529bcb5c0500a269c8ee27b87040ec96f64ef228377dc8abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068967"
---
# <a name="vertex-fog-direct3d-9"></a>Neblina de vértice (Direct3D 9)

Quando o sistema executa o vértice fogging, ele aplica cálculos de neblina em cada vértice em um polígono e, em seguida, interpola os resultados em toda a face do polígono durante a rasterização. Os efeitos de neblina de vértice são computados pelo mecanismo de iluminação e transformação de Direct3D. Para obter mais informações, consulte [parâmetros de neblina (Direct3D 9)](fog-parameters.md).

Se seu aplicativo não usar o Direct3D para transformação e iluminação, o aplicativo deverá executar cálculos de neblina. Nesse caso, coloque o fator de neblina que é calculado no componente alfa da cor especular para cada vértice. Você está livre para usar quaisquer fórmulas que desejar, com base em intervalo, volumétricos ou de outra forma. O Direct3D usa o fator de neblina fornecido para interpolar em toda a face de cada polígono. Os aplicativos que executam sua própria transformação e iluminação também devem executar seus próprios cálculos de neblina de vértice. Como resultado, tal aplicativo precisa apenas habilitar a mesclagem de neblina e definir a cor de neblina por meio dos Estados de renderização associados, conforme descrito em [fusão de neblina (Direct3D 9)](fog-blending.md) e [cor de neblina (Direct3D 9)](fog-color.md).

> [!Note]  
> Ao usar um sombreador de vértice, você deve usar a neblina de vértice. Isso é feito usando o sombreador de vértice para gravar a intensidade de neblina por vértice no registro oFog. Depois que o sombreador de pixel é concluído, os dados de oFog são usados para interpolar linearmente com a cor de neblina. Essa intensidade não está disponível em um sombreador de pixel.

 

## <a name="range-based-fog"></a>Neblina Range-Based

> [!Note]  
> O Direct3D usa cálculos de neblina com base em intervalos somente ao usar a neblina de vértice com o mecanismo de transformação e iluminação do Direct3D. Isso ocorre porque a neblina de pixel é implementada no driver de dispositivo e nenhum hardware existe atualmente para dar suporte à neblina baseada em intervalos por pixel. Se seu aplicativo executar sua própria transformação e iluminação, ele deverá executar seus próprios cálculos de neblina, baseados em intervalo ou de outra forma.

 

Às vezes, usar a neblina pode introduzir artefatos gráficos que fazem com que os objetos sejam mesclados com a cor de neblina de maneiras não intuitivas. Por exemplo, imagine uma cena na qual há dois objetos visíveis: um para cima o suficiente para ser afetado pela neblina e o outro quase suficiente para não ser afetado. Se a área de exibição for girada em vigor, os efeitos de neblinas aparentes poderão mudar, mesmo se os objetos forem estáticos. O diagrama a seguir mostra uma visão superior dessa situação.

![diagrama de dois pontos de vista e como eles afetam a neblina para dois objetos](images/artifog.png)

A neblina baseada em intervalo é outra maneira mais precisa, para determinar os efeitos de neblina. Na neblina baseada em intervalo, o Direct3D usa a distância real do ponto de vista para um vértice para seus cálculos de neblina. O Direct3D aumenta o efeito da neblina à medida que a distância entre os dois pontos aumenta, em vez da profundidade do vértice dentro da cena, evitando assim artefatos rotacionais.

Se o dispositivo atual der suporte à neblina baseada em intervalo, ele definirá o valor de FOGRANGE de D3DPRASTERCAPS \_ no membro RasterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) quando você chamar o método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) . Para habilitar a neblina baseada em intervalo, defina o \_ estado de RENDERIZAÇÃO D3DRS RANGEFOGENABLE como **true**.

A neblina baseada em intervalo é calculada pelo Direct3D durante a transformação e a iluminação. Os aplicativos que não usam o mecanismo de transformação e iluminação do Direct3D também devem executar seus próprios cálculos de neblina de vértice. Nesse caso, forneça o fator de neblina baseado em intervalo no componente alfa do componente especular para cada vértice.

## <a name="using-vertex-fog"></a>Usando a neblina de vértice

Use as etapas a seguir para habilitar a neblina de vértice em seu aplicativo.

1.  Habilite a mesclagem de neblina definindo D3DRS \_ FOGENABLE como **true**.
2.  Defina a cor de neblina no \_ estado de RENDERIZAÇÃO D3DRS FOGCOLOR.
3.  Escolha a fórmula de neblina desejada definindo o \_ estado de RENDERIZAÇÃO D3DRS FOGVERTEXMODE como um membro do tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .
4.  Defina os parâmetros de neblina conforme desejado para a fórmula de neblina selecionada nos Estados de renderização.

O exemplo a seguir, escrito em C++, mostra o que essas etapas podem parecer no código.


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



Alguns parâmetros de neblina são necessários como valores de ponto flutuante, mesmo que o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceite apenas valores DWORD no segundo parâmetro. Este exemplo fornece com êxito os valores de ponto flutuante para esses métodos sem conversão de dados, convertendo os endereços das variáveis de ponto flutuante como ponteiros DWORD e, em seguida, desreferenciando-os.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de neblina](fog-types.md)
</dt> </dl>

 

 
