---
description: Muitos aplicativos C++ limpam o buffer de profundidade antes de renderizar cada novo quadro.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Limpando buffers de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce150d729768321cb51abbea9f24ba8b490b7705f35945a4fd03e2a8ed58a039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989306"
---
# <a name="clearing-depth-buffers-direct3d-9"></a>Limpando buffers de profundidade (Direct3D 9)

Muitos aplicativos C++ limpam o buffer de profundidade antes de renderizar cada novo quadro. Você pode limpar explicitamente o buffer de profundidade por meio do Direct3D chamando [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) e especificando D3DCLEAR \_ ZBUFFER para o parâmetro flags. O método **IDirect3DDevice9:: Clear** permite que você especifique um valor de profundidade arbitrária no parâmetro Z.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de profundidade](depth-buffers.md)
</dt> </dl>

 

 
