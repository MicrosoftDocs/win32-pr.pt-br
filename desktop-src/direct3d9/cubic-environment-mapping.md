---
description: Mapas de ambiente cúbico – às vezes chamados de mapas de cubo – são texturas que contêm dados de imagem representando a cena em torno de um objeto, como se o objeto estivesse no centro de um cubo.
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: Mapeamento de ambiente cúbico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b02f86528c52c2e8e9376eb92e4452735c2613cc9b7dda08a8a07e8473193ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565308"
---
# <a name="cubic-environment-mapping-direct3d-9"></a>Mapeamento de ambiente cúbico (Direct3D 9)

Mapas de ambiente cúbico – às vezes chamados de mapas de cubo – são texturas que contêm dados de imagem representando a cena em torno de um objeto, como se o objeto estivesse no centro de um cubo. Cada face do mapa de ambiente cúbico cobre um campo de exibição de 90 graus na horizontal e na vertical, e há seis faces por mapa de cubo. A orientação das faces é mostrada na ilustração a seguir.

![ilustração de um cubo com eixos de coordenadas centrais perpendiculares a rostos de cubo](images/cubemap-cube.png)

Cada face do cubo é orientada perpendicularmente ao plano x/y, y/z ou x/z, no espaço de mundo. A ilustração a seguir mostra como cada plano corresponde a uma face.

![ilustração de rostos de cubo com projeções de coordenadas de planos](images/cube-faces.png)

Os mapas de ambiente cúbico são implementados como uma série de objetos de textura. Os aplicativos podem usar imagens estáticas para o mapeamento de ambiente cúbico ou podem renderizar nas faces do mapa do cubo para executar o mapeamento de ambiente dinâmico. Essa técnica requer que as superfícies de mapa de cubo sejam superfícies de destino de renderização válidas, criadas com o \_ sinalizador D3DUSAGE RENDERTARGET definido.

As faces de um mapa de cubo não precisam conter renderizações extremamente detalhadas da cena ao redor. Na maioria dos casos, os mapas de ambiente são aplicados a superfícies curvas. Considerando a quantidade de curvatura usada pela maioria dos aplicativos, a distorção refletida resultante faz com que detalhes extremos no mapa do ambiente sejam dispendiosos em termos de sobrecarga de memória e renderização.

## <a name="mipmapped-cubic-environment-maps"></a>Mapas de ambiente cúbico mipmapped

Os mapas de cubo podem ser mipmapped. Para criar um mapa de cubo mipmapped, defina o parâmetro níveis do método [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) como o número de níveis que você deseja. Você pode prever a topografia dessas superfícies, conforme mostrado no diagrama a seguir.

![diagrama de um mapa de cubo mipmapped com n níveis de MIP](images/cubemap-mipped.png)

Os aplicativos que criam mapas de ambiente cúbico mipmapped podem acessar cada face chamando o método [**GetCubeMapSurface**](/windows/desktop/api) . Comece definindo o valor apropriado do tipo enumerado [**D3DCUBEMAP \_ faces**](./d3dcubemap-faces.md) , conforme discutido em [criando superfícies de mapa de ambiente cúbico (Direct3D 9)](creating-cubic-environment-map-surfaces.md). Em seguida, selecione o nível a ser recuperado definindo o parâmetro de nível **GetCubeMapSurface** para o nível de mipmap que você deseja. Lembre-se de que 0 corresponde à imagem de nível superior.

## <a name="texture-coordinates-for-cubic-environment-maps"></a>Coordenadas de textura para o ambiente cúbico Mapas

As coordenadas de textura que indexam um mapa de ambiente cúbico não são coordenadas simples de u, v Style, conforme usadas quando as texturas padrão são aplicadas. Na verdade, os mapas de ambiente cúbico não usam coordenadas de textura. No lugar de um conjunto de coordenadas de textura, os mapas de ambiente cúbico exigem um vetor 3D. Você deve tomar cuidado para especificar um formato de vértice adequado. Além de informar ao sistema Quantos conjuntos de coordenadas de textura seu aplicativo usa, você deve fornecer informações sobre quantos elementos estão em cada conjunto. O Direct3D oferece o conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) para essa finalidade. Essas macros aceitam um único parâmetro, identificando o índice do conjunto de coordenadas de textura para o qual o tamanho está sendo descrito. No caso de um vetor 3D, você inclui o padrão de bits criado pela macro D3DFVF \_ TEXCOORDSIZE3. O exemplo de código a seguir mostra como essa macro é usada.


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



Em alguns casos, como o mapeamento de luz difusa, você usa o vértice de espaço de câmera normal para o vetor. Em outros casos, como o mapeamento de ambiente especular, você usa um vetor de reflexão. Como os normais de vértice transformados são amplamente compreendidos, as informações aqui se concentram em calcular um vetor de reflexo.

A computação de um vetor de reflexo por conta própria requer a compreensão da posição de cada vértice e de um vetor do ponto de vista para esse vértice. O Direct3D pode calcular automaticamente os vetores de reflexo para sua geometria. O uso desse recurso poupa memória porque você não precisa incluir coordenadas de textura para o mapa de ambiente. Ele também reduz a largura de banda e, no caso de um dispositivo de HAL T&L, ele pode ser significativamente mais rápido do que os cálculos que seu aplicativo pode fazer por conta própria. Para usar esse recurso, no estágio de textura que contém o mapa de ambiente cúbico, defina o \_ estado de estágio de textura D3DTSS TEXCOORDINDEX como uma combinação do \_ membro D3DTSS TCI \_ CAMERASPACEREFLECTIONVECTOR de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) e o índice de um conjunto de coordenadas de textura. Em algumas situações, como o mapeamento de luz difusa, você pode usar o \_ membro D3DTSS TCI \_ CAMERASPACENORMAL de **D3DTEXTURESTAGESTATETYPE**, o que faz com que o sistema use o vértice transformado, câmera-espaço, normal como o vetor de endereçamento para a textura. O índice é usado apenas pelo sistema para determinar o modo de disposição para a textura.

O exemplo de código a seguir mostra como esse valor é usado.


```
// The m_d3dDevice variable is a valid pointer
// to an IDirect3DDevice9 interface.

// Automatically generate texture coordinates for stage 2.
// This assumes that stage 2 is assigned a cube map.
// Use the wrap mode from the texture coordinate set at index 1.

m_d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX,
                                   D3DTSS_TCI_CAMERASPACEREFLECTIONVECTOR | 1); 
```



Quando você habilita a geração de coordenadas de textura automática, o sistema usa uma das duas fórmulas para calcular o vetor de reflexão para cada vértice. Quando o \_ estado de RENDERIZAÇÃO D3DRS LOCALVIEWER é definido como **true**, a fórmula a seguir é usada.

![fórmula do vetor de reflexão (r = 2 (exn) n-e)](images/reflection-vector-local.png)

Na fórmula anterior, R é o vetor de reflexo sendo computado, E é o vetor de posição-para-olho normalizado e N é o vértice de espaço de câmera normal.

Quando o \_ estado de RENDERIZAÇÃO D3DRS LOCALVIEWER é definido como **false**, o sistema usa a fórmula a seguir.

![fórmula do vetor de reflexão (r = 2nzn-i)](images/reflection-vector-nonlocal.png)

Os elementos R e N nesta fórmula são idênticos à fórmula anterior. O elemento N<sub>z</sub> é a Z de espaço Mundial do vértice normal e I é o vetor (0, 0, 1) de um ponto de vista infinitamente distante. O sistema usa o vetor de reflexo de uma das fórmulas para selecionar e tratar a face apropriada do mapa do cubo.

> [!Note]  
> Na maioria dos casos, os aplicativos devem habilitar a normalização automática de Normals de vértice. Para fazer isso, defina D3DRS \_ NORMALIZENORMALS como **true**. Se você não habilitar esse estado de renderização, a aparência do mapa de ambiente será drasticamente diferente do que você pode esperar.

 

Informações adicionais estão contidas no tópico a seguir.

-   [Criando superfícies de mapa de ambiente cúbico (Direct3D 9)](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de ambiente](environment-mapping.md)
</dt> </dl>

 

 
