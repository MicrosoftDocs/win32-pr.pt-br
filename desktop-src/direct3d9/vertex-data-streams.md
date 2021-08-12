---
description: As interfaces de renderização do Direct3D consistem em métodos que renderizar primitivos de dados de vértice armazenados em um ou mais buffers de dados.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Data Fluxos vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f154621da4ba03f78beee87767130e37da9e9ab9ba899af737b968fb20f0609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290376"
---
# <a name="vertex-data-streams-direct3d-9"></a>Data Fluxos vértice (Direct3D 9)

As interfaces de renderização do Direct3D consistem em métodos que renderizar primitivos de dados de vértice armazenados em um ou mais buffers de dados. Os dados de vértice consistem em elementos de vértice combinados para formar componentes de vértice. Os elementos de vértice, a menor unidade de um vértice, representam entidades como posição, normal ou cor.

Os componentes de vértice são um ou mais elementos de vértice armazenados contíguamente (intercalados por vértice) em um único buffer de memória. Um vértice completo consiste em um ou mais componentes, em que cada componente está em um buffer de memória separado. Para renderizar um primitivo, vários componentes de vértice são lidos e montados para que os vértices completos sejam disponibilizados para processamento de vértices. O diagrama a seguir mostra o processo de renderização de primitivos usando componentes de vértice.

![diagrama do processo para renderizar primitivos usando componentes de vértice](images/vertexdata.png)

Os primitivos de renderização consistem em duas etapas. Primeiro, configurar um ou mais fluxos de componentes de vértice; segundo, invoque [**um método IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para renderizar desses fluxos. A identificação de elementos de vértice dentro desses fluxos de componentes é especificada pelo sombreador de vértice.

Os métodos [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) especificam um deslocamento nos fluxos de dados de vértice para que um subconjunto contíguo arbitrário dos primitivos dentro de um conjunto de dados de vértice possa ser renderizado com cada invocação de desenho. Isso permite que você altere o estado de renderização do dispositivo entre grupos de primitivos renderizados dos mesmos buffers de vértice.

Há suporte para métodos de desenho indexados e não indexados. Para obter mais informações, consulte [Renderização de vértice e buffers de índice (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de primitivos](rendering-primitives.md)
</dt> </dl>

 

 
