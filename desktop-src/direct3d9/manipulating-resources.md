---
description: Seu aplicativo manipula recursos para renderizar uma cena.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Manipulando recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370033"
---
# <a name="manipulating-resources-direct3d-9"></a>Manipulando recursos (Direct3D 9)

Seu aplicativo manipula recursos para renderizar uma cena. Primeiro, um aplicativo precisa criar um recurso de textura com um dos seguintes métodos:

-   [**IDirect3DDevice9::CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

Em vez disso, um recurso de textura pode ser criado com uma das funções D3DXCreatexxx texturing.

Os objetos de textura retornados pelos métodos de criação de textura são contêineres para superfícies ou volumes; esses contêineres são genericamente conhecidos como buffers. Os buffers de Propriedade do recurso herdam os usos, o formato e o pool do recurso, mas têm seu próprio tipo. Para obter mais informações, consulte [Propriedades do recurso (Direct3D 9)](resource-properties.md).

O aplicativo obtém acesso às superfícies contidas, com a finalidade de carregar o trabalho artístico, chamando os métodos a seguir. Para obter detalhes, consulte [recursos de bloqueio (Direct3D 9)](locking-resources.md).

-   [**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [**IDirect3DVolumeTexture9:: LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

Os métodos de bloqueio assumem argumentos que indicam a superfície contida, por exemplo, o subnível mipmap ou a face do cubo dos ponteiros de textura e de retorno para os pixels. O aplicativo típico nunca usa um objeto Surface diretamente.

Crie recursos orientados a geometria chamando [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/desktop/api) ou [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).

Bloqueie e preencha os recursos de buffer chamando [**IDirect3DIndexBuffer9:: Lock**](/windows/desktop/api) ou [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), dependendo do recurso.

Para recursos de textura gerenciados, o processo de criação de recursos termina aqui. Para recursos de textura não gerenciados, um aplicativo promove recursos de memória do sistema para recursos acessíveis ao dispositivo (para aceleração de hardware) chamando [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).

Para apresentar as imagens renderizadas a partir de recursos, o aplicativo também precisa de buffers de estêncil de profundidade e cor. Para aplicativos típicos, o buffer de cores é de propriedade da cadeia de troca do dispositivo, que é uma coleção de superfícies de back-buffer e é criado implicitamente com o dispositivo. As superfícies de estêncil de profundidade podem ser criadas implicitamente ou explicitamente usando o método [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/desktop/api) . O aplicativo associa um dispositivo e seu buffer de profundidade e cor a uma chamada para [**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) ou [**IDirect3DDevice9:: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).

Para obter detalhes sobre como apresentar a imagem final, consulte [apresentação de uma cena (Direct3D 9)](presenting-a-scene.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
