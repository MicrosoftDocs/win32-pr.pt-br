---
title: Como inicializar uma textura programaticamente
description: Este tópico tem vários exemplos que mostram como inicializar texturas criadas com diferentes tipos de usos.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b7d34e7e85fd647a6f45c93d61b3330825261f59d87b9c13a95547e742e365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530558"
---
# <a name="how-to-initialize-a-texture-programmatically"></a>Como: inicializar uma textura programaticamente

Você pode inicializar uma textura durante a criação do objeto ou pode preencher o objeto programaticamente após sua criação. Este tópico tem vários exemplos que mostram como inicializar texturas criadas com diferentes tipos de usos. Este exemplo pressupõe que você já sabe como [criar uma textura](overviews-direct3d-11-resources-textures-create.md).

-   [Uso padrão](#default-usage)
-   [Uso dinâmico](#dynamic-usage)
-   [Uso de preparo](#staging-usage)
-   [Tópicos relacionados](#related-topics)

## <a name="default-usage"></a>Uso padrão

O tipo de uso mais comum é o uso padrão. Para preencher uma textura padrão (uma criada com **o \_ \_ padrão de uso D3D11**), você pode:

-   Chame [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e inicialize *pInitialData* para apontar para os dados fornecidos de um aplicativo.

    ou

-   Depois de chamar [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), use [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) para preencher a textura padrão com dados de um ponteiro fornecido pelo aplicativo.

## <a name="dynamic-usage"></a>Uso dinâmico

Para preencher uma textura dinâmica (uma criada com **D3D11 \_ uso \_ dinâmico**):

1.  Obtenha um ponteiro para a memória de textura passando no **D3D11 \_ map \_ Write \_ Discard** ao chamar [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Grave dados na memória.
3.  Chame [**ID3D11DeviceContext:: Inmapear**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) quando terminar de gravar dados.

## <a name="staging-usage"></a>Uso de preparo

Para preencher uma textura de preparo (uma criada com **o \_ \_ preparo de uso do D3D11**):

1.  Obtenha um ponteiro para a memória de textura passando a **\_ \_ gravação do mapa D3D11** ao chamar [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Grave dados na memória.
3.  Chame [**ID3D11DeviceContext:: Inmapear**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) quando terminar de gravar dados.

Uma textura de preparo pode ser usada como o parâmetro de origem para [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) ou [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) para preencher um recurso padrão ou dinâmico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




