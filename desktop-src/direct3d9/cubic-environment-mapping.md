---
description: Mapas de ambiente cúbica , às vezes chamados de mapas de cubo, são texturas que contêm dados de imagem que representam a cena em torno de um objeto, como se o objeto estivesse no centro de um cubo.
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: Mapeamento de ambiente cúbica (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b02f86528c52c2e8e9376eb92e4452735c2613cc9b7dda08a8a07e8473193ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565308"
---
# <a name="cubic-environment-mapping-direct3d-9"></a>Mapeamento de ambiente cúbica (Direct3D 9)

Mapas de ambiente cúbica , às vezes chamados de mapas de cubo, são texturas que contêm dados de imagem que representam a cena em torno de um objeto, como se o objeto estivesse no centro de um cubo. Cada face do mapa de ambiente cúbica abrange um campo de exibição de 90 graus no horizontal e vertical e há seis faces por mapa de cubo. A orientação das faces é mostrada na ilustração a seguir.

![ilustração de um cubo com eixos de coordenadas centrais – faces de cubo](images/cubemap-cube.png)

Cada face do cubo é orientada ao plano x/y, y/z ou x/z, no espaço do mundo. A ilustração a seguir mostra como cada plano corresponde a um rosto.

![ilustração de rostos de cubo com projeções de coordenadas de planos](images/cube-faces.png)

Mapas de ambiente cúbica são implementados como uma série de objetos de textura. Os aplicativos podem usar imagens estáticas para mapeamento de ambiente cúbica ou renderizar nos rostos do mapa de cubo para executar o mapeamento dinâmico de ambiente. Essa técnica requer que as superfícies de mapa de cubo sejam superfícies de destino de renderização válidas, criadas com o sinalizador RENDERTARGET D3DUSAGE \_ definido.

As faces de um mapa de cubo não precisam conter renderizações extremamente detalhadas da cena ao redor. Na maioria dos casos, os mapas de ambiente são aplicados a superfícies curvadas. Considerando a quantidade de curvatura usada pela maioria dos aplicativos, a distorção reflexiva resultante torna extremamente detalhado o desperdício no mapa do ambiente em termos de memória e sobrecarga de renderização.

## <a name="mipmapped-cubic-environment-maps"></a>Mapas

Mapas de cubo podem ser mapeados. Para criar um mapa de cubo mapeado mipmapped, de definido o parâmetro Levels do [**método CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) como o número de níveis que você deseja. Você pode prever a topografia dessas superfícies, conforme mostrado no diagrama a seguir.

![diagrama de um mapa de cubo mapeado com n níveis de mip](images/cubemap-mipped.png)

Aplicativos que criam mapas de ambiente cúbica mapeados em mipmapped podem acessar cada rosto chamando o [**método GetCubeMapSurface.**](/windows/desktop/api) Comece definindo o valor apropriado do tipo enumerado [**D3DCUBEMAP \_ FACES,**](./d3dcubemap-faces.md) conforme discutido em Criando superfícies de mapa de ambiente cúbica [(Direct3D 9)](creating-cubic-environment-map-surfaces.md). Em seguida, selecione o nível a ser recuperado definindo o parâmetro de nível **GetCubeMapSurface** para o nível de mipmap que você deseja. Lembre-se de que 0 corresponde à imagem de nível superior.

## <a name="texture-coordinates-for-cubic-environment-maps"></a>Coordenadas de textura para ambiente cúbica Mapas

As coordenadas de textura que indexam um mapa de ambiente cúbica não são coordenadas simples de estilo u, v, como usadas quando texturas padrão são aplicadas. Na verdade, os mapas de ambiente cúbica não usam coordenadas de textura. No lugar de um conjunto de coordenadas de textura, os mapas de ambiente cúbica exigem um vetor 3D. Você deve tomar cuidado para especificar um formato de vértice adequado. Além de dizer ao sistema quantos conjuntos de coordenadas de textura seu aplicativo usa, você deve fornecer informações sobre quantos elementos estão em cada conjunto. O Direct3D oferece o conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) para essa finalidade. Essas macros aceitam um único parâmetro, identificando o índice do conjunto de coordenadas de textura para o qual o tamanho está sendo descrito. No caso de um vetor 3D, você inclui o padrão de bit criado pela macro D3DFVF \_ TEXCOORDSIZE3. O exemplo de código a seguir mostra como essa macro é usada.


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



Em alguns casos, como mapeamento de luz difuso, você usa o vértice de espaço da câmera normal para o vetor. Em outros casos, como o mapeamento de ambiente especular, você usa um vetor de reflexão. Como os normais de vértice transformados são amplamente compreendidos, as informações aqui se concentram na computação de um vetor de reflexão.

A computação de um vetor de reflexão por conta própria requer a compreensão da posição de cada vértice e de um vetor do ponto de vista para esse vértice. O Direct3D pode calcular automaticamente os vetores de reflexão para sua geometria. O uso desse recurso economiza memória porque você não precisa incluir coordenadas de textura para o mapa de ambiente. Ele também reduz a largura de banda e, no caso de um dispositivo T&L HAL, ele pode ser significativamente mais rápido do que os cálculos que seu aplicativo pode fazer por conta própria. Para usar esse recurso, no estágio de textura que contém o mapa de ambiente cúbica, de definir o estado do estágio de textura DE TEXCOORDINDEX de D3DTSS como uma combinação do membro \_ \_ \_ CAMERASPACEREFLECTIONVECTOR de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) e o índice de um conjunto de coordenadas de textura. Em algumas situações, como o mapeamento difuso de luz, você pode usar o membro \_ CAMERASPACENORMAL do TCI D3DTSS \_ de **D3DTEXTURESTAGESTATETYPE**, que faz com que o sistema use o vértice transformado, o espaço da câmera, o vértice normal como o vetor de endereçamento para a textura. O índice só é usado pelo sistema para determinar o modo de empacotamento para a textura.

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



Quando você habilita a geração automática de coordenadas de textura, o sistema usa uma das duas fórmulas para calcular o vetor de reflexão para cada vértice. Quando o estado de renderização LOCALVIEWER D3DRS é \_ definido como **TRUE,** a fórmula a seguir é usada.

![fórmula do vetor de reflexão (r = 2(exn)n-e)](images/reflection-vector-local.png)

Na fórmula anterior, R é o vetor de reflexão que está sendo calculado, E é o vetor de posição para o olho normalizado e N é o vértice de espaço da câmera normal.

Quando o estado de renderização LOCALVIEWER D3DRS é \_ definido como **FALSE,** o sistema usa a fórmula a seguir.

![fórmula do vetor de reflexão (r = 2nzn-i)](images/reflection-vector-nonlocal.png)

Os elementos R e N nesta fórmula são idênticos à fórmula anterior. O elemento N<sub>Z</sub> é o espaço do mundo z do vértice normal e eu é o vetor (0,0,1) de um ponto de vista infinitamente distante. O sistema usa o vetor de reflexão de qualquer fórmula para selecionar e abordar o rosto apropriado do mapa de cubo.

> [!Note]  
> Na maioria dos casos, os aplicativos devem habilitar a normalização automática de normais de vértice. Para fazer isso, de definir D3DRS \_ NORMALIZENORMALS como **TRUE.** Se você não habilitar esse estado de renderização, a aparência do mapa do ambiente será drasticamente diferente do esperado.

 

Informações adicionais estão contidas no tópico a seguir.

-   [Criando superfícies de mapa de ambiente cúbica (Direct3D 9)](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de ambiente](environment-mapping.md)
</dt> </dl>

 

 
