---
description: Agora você pode criar automaticamente um mipmap que é uma série de texturas, cada uma filtrada para uma resolução diferente.
ms.assetid: ae5955f9-e52a-41d7-a199-800e37a3e936
title: Geração automática de mipmaps (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fda5b765d42ffa10f8cc5998daa66ae36c2bc75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784582"
---
# <a name="automatic-generation-of-mipmaps-direct3d-9"></a>Geração automática de mipmaps (Direct3D 9)

Agora você pode criar automaticamente um mipmap que é uma série de texturas, cada uma filtrada para uma resolução diferente. Mipmaps são normalmente usados para fornecer diferentes níveis de detalhes durante a renderização. A geração automática de mipmaps no momento da criação da textura tira proveito da filtragem de hardware porque o mipmap reside na memória de vídeo.

Para gerar um mipmap automaticamente, defina um novo uso [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) antes de chamar [**CreateTexture**](/windows/desktop/api). A geração de subnível desse ponto em é completamente transparente para o aplicativo. Somente o nível de textura superior pode ser acessado pelo aplicativo; os subníveis de textura não estão acessíveis, pois eles serão criados somente quando necessário pelo driver. Nos casos em que a geração de subnível pode demorar muito tempo, use [**GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) para indicar ao driver que ele deve gerar subníveis de cada vez, apropriado para o aplicativo.

## <a name="mipmap-filtering"></a>Filtragem de mipmap

[**SetAutoGenFilterType**](/windows/desktop/api) controla a qualidade da filtragem durante a geração automática. Alterar o tipo de filtro sujeira os subníveis mipmap e faz com que eles sejam regenerados. Use [**GetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getautogenfiltertype) para obter o tipo de filtro atual. O tipo de filtro padrão é D3DTEXF \_ linear. Se o driver não oferecer suporte a um filtro linear, o tipo de filtro será definido como D3DTEXF \_ Point.

Esses métodos não terão efeito se a textura não for criada com [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) e nenhuma falha for retornada. Todos os tipos de filtro com suporte do driver para filtragem de textura regular têm suporte para gerado automaticamente, exceto D3DTEXF \_ None. Para cada tipo de recurso, os drivers devem dar suporte a todos os tipos de filtro relatados nas Caps de filtro de textura, CubeTexture e volumetexture correspondentes.

Para verificar quais tipos de filtro têm suporte, verifique quais caps são suportados pelos membros TextureFilterCaps e/ou CubeTextureFilterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="mipmap-support"></a>Suporte do mipmap

[D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) é apenas uma dica e especificar isso durante a criação de textura ou ao chamar [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) não causaria um erro em nenhum dos tipos de DDI (interface de driver de dispositivo).

Chamar [**UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) é inválido quando a origem é um mipmap gerado automaticamente, mas o destino não é. A origem pode ser um mipmap não gerado automaticamente e o destino pode ser um mipmap gerado automaticamente. Nesse caso, somente o nível de correspondência mais alto é atualizado. Todos os outros subníveis de origem são ignorados. Da mesma forma, quando a origem e o destino são gerados automaticamente, somente o nível de correspondência mais alto é atualizado. Os subníveis da origem são ignorados e os subníveis de destino são regenerados.

Para verificar o suporte à geração automática de mipmaps, verifique se [D3DCAPS2 \_ CANAUTOGENMIPMAP](d3dcaps2.md) está definido. Se for, chame [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) com [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md). Se o valor de retorno for D3D \_ OK, os mipmaps terão a garantia de serem gerados automaticamente. Se o valor de retorno for D3DOK \_ NOAUTOGEN, isso significará que a chamada de criação terá sucesso, mas não haverá nenhum mipmaps gerado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas do Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
