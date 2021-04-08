---
description: Os dispositivos Direct3D podem transformar as coordenadas de textura para vértices aplicando uma matriz 4x4.
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: Transformações de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45b8107f609348ae2367b1171ae7913797f4558
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087588"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a>Transformações de coordenadas de textura (Direct3D 9)

Os dispositivos Direct3D podem transformar as coordenadas de textura para vértices aplicando uma matriz 4x4. O sistema aplica transformações a coordenadas de textura da mesma maneira que a geometria. Qualquer transformação (escala, rotação, tradução, projeção, distorção ou qualquer combinação desses) pode ser feita com uma matriz 4x4.

> [!Note]  
> O Direct3D não modifica os vértices transformados e acesos. Como resultado, um aplicativo que usa vértices transformados e acesos não pode usar o Direct3D para transformar as coordenadas de textura dos vértices.

 

Dispositivos que dão suporte a operações de transformação e iluminação aceleradas por hardware (T&L dispositivo HAL) também aceleram a transformação de coordenadas de textura. Quando a aceleração de hardware das transformações não está disponível, as otimizações específicas da plataforma no pipeline do Direct3D Geometry se aplicam às transformações de coordenadas de textura.

As transformações de coordenadas de textura são úteis para produzir efeitos especiais e, ao mesmo tempo, evitar a necessidade de modificar diretamente as coordenadas de textura de sua geometria. Você pode usar matrizes de conversão simples ou de rotação para animar texturas em um objeto ou pode transformar coordenadas de textura geradas automaticamente pelo Direct3D para simplificar e, talvez, acelerar os efeitos avançados, como texturas projetadas e mapeamento claro dinâmico. Além disso, você pode usar transformações de coordenadas de textura para reutilizar um único conjunto de coordenadas de textura para várias finalidades, em vários estágios de textura.

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>Configurando e recuperando transformações de coordenadas de textura

Assim como as matrizes que seu aplicativo usa para geometria, você define e recupera transformações de coordenadas de textura chamando os métodos [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) e [**IDirect3DDevice9:: GetTransform**](/windows/desktop/api) . Esses métodos aceitam os \_ membros de D3DTS TEXTURE0 por meio \_ de D3DTS TEXTURE7 do tipo enumerado [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) para identificar as matrizes de transformação de estágios de textura de 0 a 7, respectivamente.

O código a seguir define uma matriz a ser aplicada às coordenadas de textura para o estágio 0 da textura.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>Habilitando transformações de coordenadas de textura

O \_ estado de estágio de textura D3DTSS TEXTURETRANSFORMFLAGS controla o aplicativo de transformações de coordenadas de textura. Os valores para esse estado de estágio de textura são definidos pelo tipo enumerado [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) .

As transformações de coordenadas de textura são desabilitadas quando D3DTSS \_ TEXTURETRANSFORMFLAGS é definido como D3DTTFF \_ Disable (o valor padrão). Supondo que as transformações da coordenada de textura foram habilitadas para o estágio 0, o código a seguir as desabilitará.


```
// For this example, assume the d3dDevice variable contains a 
// valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_DISABLE );
```



Os outros valores definidos em [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) são usados para habilitar transformações de coordenadas de textura e para controlar quantos elementos de coordenadas de textura resultantes são passados para o rasterizador. Por exemplo, use o código a seguir.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT2 );
```



O \_ valor D3DTTFF COUNT2 instrui o sistema a aplicar a matriz de transformação definida para o estágio 0 da textura e, em seguida, passar os dois primeiros elementos das coordenadas de textura modificadas para o rasterizador.

O \_ sinalizador de transformação de textura projetada D3DTTFF indica coordenadas para uma textura projetada. Quando esse sinalizador é especificado, o rasterizador divide os elementos passados pelo último elemento. Use o código a seguir, por exemplo.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT3 | D3DTTFF_PROJECTED );
```



Este exemplo informa o sistema para passar três elementos de coordenadas de textura para o rasterizador. O rasterizador divide os dois primeiros elementos pela terceira, produzindo as coordenadas de textura 2D necessárias para tratar a textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processamento de coordenadas de textura](texture-coordinate-processing.md)
</dt> </dl>

 

 
