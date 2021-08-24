---
description: Ao usar um sombreador de vértice programado, os elementos atualizados no buffer de vértice de destino são controlados pelo programa de funções do sombreador.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Processamento programável de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ee1e781aa811d8d85a8865bdf07a8811e26d027f6d385b40126a8321172a3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118586"
---
# <a name="programmable-vertex-processing-direct3d-9"></a>Processamento programável de vértice (Direct3D 9)

Ao usar um sombreador de vértice programado, os elementos atualizados no buffer de vértice de destino são controlados pelo programa de funções do sombreador. Quando o aplicativo grava em um dos registros de vértice de destino, o elemento correspondente dentro de cada vértice do buffer de vértice de destino é atualizado. Elementos no buffer de vértice de destino que não são gravados pelo aplicativo não são modificados. [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) falhará se o aplicativo grava em elementos que não estão presentes no buffer de vértice de destino.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de vértice](vertex-buffers.md)
</dt> </dl>

 

 
