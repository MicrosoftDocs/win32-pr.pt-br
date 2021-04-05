---
description: As interfaces de renderização para o Direct3D consistem em métodos que processam primitivos de dados de vértice armazenados em um ou mais buffers de dados.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Fluxos de dados de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645800"
---
# <a name="vertex-data-streams-direct3d-9"></a>Fluxos de dados de vértice (Direct3D 9)

As interfaces de renderização para o Direct3D consistem em métodos que processam primitivos de dados de vértice armazenados em um ou mais buffers de dados. Os dados de vértice consistem em elementos de vértice combinados para formar componentes de vértice. Os elementos Vertex, a menor unidade de um vértice, representam entidades como position, normal ou Color.

Os componentes de vértice são um ou mais elementos de vértice armazenados de forma contígua (intercalados por vértice) em um único buffer de memória. Um vértice completo consiste em um ou mais componentes, onde cada componente está em um buffer de memória separado. Para renderizar um primitivo, vários componentes de vértice são lidos e montados para que os vértices completos estejam disponíveis para processamento de vértice. O diagrama a seguir mostra o processo de renderização de primitivos usando componentes de vértice.

![diagrama do processo para renderizar primitivos usando componentes de vértice](images/vertexdata.png)

Os primitivos de renderização consistem em duas etapas. Primeiro, configure um ou mais fluxos de componentes de vértice; em segundo lugar, invoque um método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para renderizar desses fluxos. A identificação dos elementos de vértice dentro desses fluxos de componente é especificada pelo sombreador de vértice.

Os métodos [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) especificam um deslocamento nos fluxos de dados de vértice para que um subconjunto contíguo arbitrário dos primitivos dentro de um conjunto de dados de vértice possa ser renderizado com cada invocação de desenho. Isso permite que você altere o estado de renderização do dispositivo entre grupos de primitivos que são processados dos mesmos buffers de vértice.

Há suporte para métodos de desenho indexados e não indexados. Para obter mais informações, consulte [renderizando de vértices e buffers de índice (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos de renderização](rendering-primitives.md)
</dt> </dl>

 

 
