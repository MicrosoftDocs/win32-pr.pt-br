---
description: Quando o Direct3D renderiza uma primitiva, ele mapeia a primitiva 3D em uma tela 2D.
ms.assetid: vs|directx_sdk|~\texture_filtering.htm
title: Filtragem de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758ee51df65ffa4dddf793db83fe618107886cd4c20497f0e8090373a1415beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291171"
---
# <a name="texture-filtering-direct3d-9"></a>Filtragem de textura (Direct3D 9)

Quando o Direct3D renderiza uma primitiva, ele mapeia a primitiva 3D em uma tela 2D. Se a primitiva tem uma textura, o Direct3D deve usar essa textura para produzir uma cor para cada pixel na imagem renderizada em 2D da primitiva. Para cada pixel da imagem na tela da primitiva, ele deve obter um valor de cor da textura. Esse processo é chamado de filtragem de textura.

Quando uma operação de filtro de textura é executada, a textura que está sendo usada normalmente também está sendo ampliada ou reduzida. Em outras palavras, ela está sendo mapeada para uma imagem primitiva maior ou menor que ela mesma. A ampliação de uma textura pode resultar no mapeamento de muitos pixels para um texel. O resultado pode ser uma aparência robusta. A redução de uma textura geralmente significa que um único pixel é mapeado para muitos texels. A imagem resultante pode ficar desfocada ou distorcida. Para resolver esses problemas, a mesclagem das cores dos texels devem ser realizada para chegar a uma cor para o pixel.

O Direct3D simplifica o processo complexo de filtragem de textura. Ele fornece três tipos de filtragem de textura: filtragem linear, filtragem anisotrópica e filtragem mipmap. Se você não selecionar a filtragem de textura, o Direct3D usará uma técnica chamada de amostragem do ponto mais próximo.

Cada tipo de filtragem de textura possui vantagens e desvantagens. Por exemplo, a filtragem de textura linear pode produzir bordas irregulares ou uma aparência robusta na imagem final. No entanto, esse é um método de filtragem de textura computacionalmente de baixa sobrecarga. A filtragem com mipmaps geralmente produz os melhores resultados, especialmente quando combinada com uma filtragem anisotrópica. No entanto, ele exige o máximo de memória das técnicas que o Direct3D pode suportar.

Os aplicativos que usam ponteiros de interface de textura devem definir o método de filtragem de textura atual chamando o método [**IDirect3DDevice9:: Setsamplestate**](/windows/desktop/api) . Defina o valor do primeiro parâmetro como o número de índice inteiro (0-7) da textura para a qual você está selecionando um método de filtragem de textura. Pass D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER ou D3DSAMP \_ MIPFILTER para o segundo parâmetro para definir o filtro de ampliação, minificação ou mipmapping. Passe um membro do tipo enumerado [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) como o valor no terceiro parâmetro.

Esta seção apresenta os métodos de filtragem de textura para os quais o Direct3D dá suporte. Ele é organizado nos tópicos a seguir.

-   [Amostragem de ponto mais próximo (Direct3D 9)](nearest-point-sampling.md)
-   [Filtragem de textura linear (Direct3D 9)](linear-texture-filtering.md)
-   [Filtragem de textura bilinear (Direct3D 9)](bilinear-texture-filtering.md)
-   [Filtragem de textura anisotropic (Direct3D 9)](anisotropic-texture-filtering.md)
-   [Filtragem de textura com mipmaps (Direct3D 9)](texture-filtering-with-mipmaps.md)

> [!Note]  
> Embora os Estados de renderização de filtragem de textura presentes no tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) sejam substituídos pelos Estados de estágio de textura, o [**IDirect3DDevice9:: setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate), em oposição à versão do IDirect3DDevice2, não falhará se você tentar usá-los. Em vez disso, o sistema mapeia os efeitos desses Estados de renderização para o primeiro estágio na cascata multitextura, estágio 0. Os aplicativos não devem misturar os Estados de renderização herdados com seus Estados de estágio de textura correspondentes, pois podem ocorrer resultados imprevisíveis.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas do Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
