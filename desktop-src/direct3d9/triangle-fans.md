---
description: Um ventilador de triângulo é semelhante a uma faixa de triângulo, exceto que todos os triângulos compartilham um vértice, conforme mostrado na ilustração a seguir.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Ventiladores de triângulo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806dc57545f4cb8341eee2b586aa062ba93d98568e6269e209dbf616fbb081d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044164"
---
# <a name="triangle-fans-direct3d-9"></a>Ventiladores de triângulo (Direct3D 9)

Um ventilador de triângulo é semelhante a uma faixa de triângulo, exceto que todos os triângulos compartilham um vértice, conforme mostrado na ilustração a seguir.

![ilustração de um ventilador de triângulo](images/trifan.gif)

O sistema usa v2, v3 e v1 para desenhar o primeiro triângulo; v3, v4 e v1 para desenhar o segundo triângulo; v4, v5 e v1 para desenhar o terceiro triângulo; e assim por diante. Quando o sombreamento simples está habilitado, o sistema sombrea o triângulo com a cor de seu primeiro vértice.

A ilustração a seguir ilustra um ventilador de triângulo renderizado.

![ilustração de um ventilador de triângulo renderizado](images/tfan2.gif)

O código a seguir mostra como criar vértices para esse ventilador de triângulo.


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



O exemplo de código abaixo mostra como renderizar esse ventilador de triângulo no Direct3D 9 usando [**IDirect3DDevice9::D rawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



Não há suporte para ventiladores de triângulo no Direct3D 10 ou posterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos](primitives.md)
</dt> </dl>

 

 
