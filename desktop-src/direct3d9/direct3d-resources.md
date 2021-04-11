---
description: Os recursos são as texturas e os buffers que são usados para renderizar uma cena.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Recursos do Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7745318db3d880711ee962edb086996764455ec8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087598"
---
# <a name="direct3d-resources-direct3d-9"></a>Recursos do Direct3D (Direct3D 9)

Os recursos são as texturas e os buffers que são usados para renderizar uma cena. Os aplicativos precisam criar, carregar, copiar e usar recursos. Esta seção fornece uma breve introdução aos recursos e às etapas e aos métodos usados por aplicativos ao trabalhar com recursos.

Todos os recursos, incluindo os recursos de geometria [**IDirect3DIndexBuffer9**](/windows/desktop/api) e [**IDirect3DVertexBuffer9**](/windows/desktop/api), herdam da interface [**IDirect3DResource9**](/windows/desktop/api) . Os recursos de textura, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)e [**IDirect3DVolumeTexture9**](/windows/desktop/api), também herdam da interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) .

-   [Propriedades do recurso (Direct3D 9)](resource-properties.md)
-   [Manipulando recursos (Direct3D 9)](manipulating-resources.md)
-   [Recursos de bloqueio (Direct3D 9)](locking-resources.md)
-   [Relações de recursos (Direct3D 9)](resource-relationships.md)
-   [Gerenciando recursos (Direct3D 9)](managing-resources.md)
-   [Recursos gerenciados por aplicativo e estratégias de alocação (Direct3D 9)](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [Buffers de índice (Direct3D 9)](index-buffers.md)
-   [Buffers de vértice (Direct3D 9)](vertex-buffers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> </dl>

 

 
