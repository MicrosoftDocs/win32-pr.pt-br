---
description: Muitos aplicativos C++ limpam o buffer de profundidade antes de renderizar cada novo quadro.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Limpando buffers de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ad415b5c92e62da4f64eb590a0e202ffa3e0c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793635"
---
# <a name="clearing-depth-buffers-direct3d-9"></a>Limpando buffers de profundidade (Direct3D 9)

Muitos aplicativos C++ limpam o buffer de profundidade antes de renderizar cada novo quadro. Você pode limpar explicitamente o buffer de profundidade por meio do Direct3D chamando [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) e especificando D3DCLEAR \_ ZBUFFER para o parâmetro flags. O método **IDirect3DDevice9:: Clear** permite que você especifique um valor de profundidade arbitrária no parâmetro Z.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de profundidade](depth-buffers.md)
</dt> </dl>

 

 
