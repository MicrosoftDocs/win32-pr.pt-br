---
description: Ao usar um sombreador de vértice programado, os elementos atualizados no buffer de vértice de destino são controlados pelo programa de funções do sombreador.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Processamento de vértice programável (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108792350aebbca4f58924fde81d191b062591b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105811460"
---
# <a name="programmable-vertex-processing-direct3d-9"></a>Processamento de vértice programável (Direct3D 9)

Ao usar um sombreador de vértice programado, os elementos atualizados no buffer de vértice de destino são controlados pelo programa de funções do sombreador. Quando o aplicativo grava em um dos registros de vértice de destino, o elemento correspondente dentro de cada vértice do buffer de vértice de destino é atualizado. Os elementos no buffer de vértice de destino que não são gravados pelo aplicativo não são modificados. [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) falhará se o aplicativo gravar em elementos que não estão presentes no buffer de vértice de destino.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de vértice](vertex-buffers.md)
</dt> </dl>

 

 
