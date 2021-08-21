---
description: Um primitivo 3D é uma coleção de vértices que forma uma única entidade 3D. A primitiva mais simples é uma coleção de pontos em um sistema de coordenadas 3D, que é chamada de lista de pontos.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Primitivos (gráficos do Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af846ded9798a25238287be7dd017dcf6efecdfb2976723638881c7e00f9642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092549"
---
# <a name="primitives-direct3d-9-graphics"></a>Primitivos (gráficos do Direct3D 9)

Um primitivo 3D é uma coleção de vértices que forma uma única entidade 3D. A primitiva mais simples é uma coleção de pontos em um sistema de coordenadas 3D, que é chamada de lista de pontos.

Geralmente, os primitivos 3D são polígonos. Um polígono é uma figura 3D fechada delineada por pelo menos três vértices. O polígono mais simples é um triângulo. O Microsoft Direct3D usa triângulos para compor a maior parte de seus polígonos porque é garantido que todos os três vértices de um triângulo serão coplanares. Renderizar vértices que não são planares é ineficiente. Você pode combinar triângulos para formar malhas e polígonos grandes e complexos.

A ilustração a seguir mostra um cubo. Dois triângulos formam cada face do cubo. Todo o conjunto de triângulos constitui um primitivo cúbico. Você pode aplicar texturas e materiais às superfícies de primitivos para que pareçam ser um único Formulário sólido. Para obter detalhes, confira [materiais (Direct3D 9)](materials.md) e [texturas do Direct3D (Direct3D 9)](direct3d-textures.md).

![ilustração de um cubo com dois triângulos em cada face](images/cube3d.png)

Você também pode usar triângulos para criar primitivos cujas superfícies parecem ser curvas suaves. A ilustração a seguir mostra como uma esfera pode ser simulada com triângulos. Depois que um material é aplicado, a esfera é curvada quando é renderizada. Isso é especialmente verdadeiro se você usar o sombreamento Gouraud. Para obter detalhes, consulte [sombreamento Gouraud](shading-modes.md).

![ilustração de uma esfera simulada usando triângulos](images/sphere3d.png)

Os dispositivos Direct3D podem criar e manipular os seguintes tipos de primitivos.

-   [Listas de pontos](point-lists.md)
-   [Listas de linhas](line-lists.md)
-   [Faixas de linha](line-strips.md)
-   [Listas de triângulo](triangle-lists.md)
-   [Faixas de triângulo](triangle-strips.md)
-   [Ventiladores de triângulo (Direct3D 9)](triangle-fans.md)

Você pode renderizar tipos primitivos de um aplicativo C++ com qualquer um dos métodos de renderização da interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
