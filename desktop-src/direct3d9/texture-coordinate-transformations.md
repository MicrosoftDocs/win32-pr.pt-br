---
description: Os dispositivos Direct3D podem transformar as coordenadas de textura para vértices aplicando uma matriz 4x4.
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: Transformações de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755af38c6c58fc2f19297b056e3e9f35ce2559a6a7a2d52e8a23c94f93f4fbaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984786"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a>Transformações de coordenadas de textura (Direct3D 9)

Os dispositivos Direct3D podem transformar as coordenadas de textura para vértices aplicando uma matriz 4x4. O sistema aplica transformações às coordenadas de textura da mesma maneira que a geometria. Qualquer transformação (escala, rotação, tradução, projeção, csa ou qualquer combinação deles) pode ser feita com uma matriz 4x4.

> [!Note]  
> O Direct3D não modifica os vértices transformados e acesos. Como resultado, um aplicativo que usa vértices transformados e acesos não pode usar o Direct3D para transformar as coordenadas de textura dos vértices.

 

Dispositivos que suportam operações de transformação e iluminação aceleradas por hardware (T&dispositivo L HAL) também aceleram a transformação de coordenadas de textura. Quando a aceleração de hardware de transformações não está disponível, otimizações específicas da plataforma no pipeline de geometria Direct3D se aplicam a transformações de coordenadas de textura.

Transformações de coordenadas de textura são úteis para produzir efeitos especiais, evitando a necessidade de modificar diretamente as coordenadas de textura da geometria. Você pode usar matrizes simples de conversão ou rotação para animar texturas em um objeto ou transformar coordenadas de textura geradas automaticamente pelo Direct3D para simplificar e talvez acelerar efeitos avançados, como texturas projetadas e mapeamento dinâmico de luz. Além disso, você pode usar as transformação de coordenadas de textura para reutilizar um único conjunto de coordenadas de textura para várias finalidades, em vários estágios de textura.

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>Configurando e recuperando transformações de coordenadas de textura

Assim como as matrizes que seu aplicativo usa para geometria, você definirá e recuperará transformações de coordenadas de textura chamando os métodos [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) e [**IDirect3DDevice9::GetTransform.**](/windows/desktop/api) Esses métodos aceitam os membros TEXTURE0 de D3DTS por \_ meio de D3DTS TEXTURE7 do tipo \_ enumerado [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) para identificar as matrizes de transformação para estágios de textura de 0 a 7, respectivamente.

O código a seguir define uma matriz a ser aplicada às coordenadas de textura para o estágio de textura 0.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>Habilitando transformações de coordenadas de textura

O estado do estágio de textura \_ TEXTURETRANSFORMFLAGS D3DTS controla a aplicação de transformações de coordenadas de textura. Os valores para esse estado de estágio de textura são definidos pelo tipo enumerado [**D3DTEXTURETRANSFORMFLAGS.**](./d3dtexturetransformflags.md)

As transformações de coordenadas de textura são desabilitadas quando \_ TEXTURETRANSFORMFLAGS D3DTSS é definido como D3DTTFF \_ DISABLE (o valor padrão). Supondo que as transformações de coordenadas de textura foram habilitadas para o estágio 0, o código a seguir as desabilita.


```
// For this example, assume the d3dDevice variable contains a 
// valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_DISABLE );
```



Os outros valores definidos em [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) são usados para habilitar transformações de coordenadas de textura e para controlar quantos elementos de coordenadas de textura resultantes são passados para o rasterizador. Por exemplo, pegue o código a seguir.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT2 );
```



O valor D3DTTFF COUNT2 instrui o sistema a aplicar o conjunto de matrizes de transformação para o estágio de textura 0 e, em seguida, passar os dois primeiros elementos das coordenadas de textura modificadas para o \_ rasterizador.

O sinalizador de transformação de textura PROJECTED D3DTTFF \_ indica coordenadas para uma textura projetada. Quando esse sinalizador é especificado, o rasterizador divide os elementos passados pelo último elemento. Pegue o código a seguir, por exemplo.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT3 | D3DTTFF_PROJECTED );
```



Este exemplo informa ao sistema para passar três elementos de coordenadas de textura para o rasterizador. O rasterizador divide os dois primeiros elementos pelo terceiro, produzindo as coordenadas de textura 2D necessárias para lidar com a textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processamento de coordenadas de textura](texture-coordinate-processing.md)
</dt> </dl>

 

 
