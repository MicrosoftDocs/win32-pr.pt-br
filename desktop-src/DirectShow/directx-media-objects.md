---
description: Objetos de mídia do DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Objetos de mídia do DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ef7dc17ab595748d9ccbfa16e33e7b4b8057d161c7f1e5d9f589e6768ec35f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821191"
---
# <a name="directx-media-objects"></a>Objetos de mídia do DirectX

> [!Note]  
> Os DMOs foram superados por Media Foundation transformação (MFTs). [](/windows/desktop/medfound/media-foundation-transforms) Ainda há DMO interfaces de rede. No entanto, se você estiver escrevendo um plug-in de processamento de codec ou áudio/vídeo personalizado, considere implementá-lo como um MFT.

 

Os DMOs (Objetos de Mídia DirectX) são componentes de streaming de dados baseados em COM. Em alguns aspectos, os DMOs são semelhantes aos filtros DirectShow Microsoft. Como DirectShow filtros, os DMOs usam dados de entrada para produzir dados de saída. No entanto, as APIs (interfaces de programação de aplicativo) para DMOs são muito mais simples do que as APIs correspondentes para DirectShow. Como resultado, os DMOs são mais fáceis de criar, testar e usar. Os DMOs podem ser usados em muitos cenários:

-   Aplicativos baseados DirectShow podem usar DMOs por meio de um filtro DirectShow chamado filtro [DMO Wrapper.](dmo-wrapper-filter.md) A distinção entre filtros e DMOs é transparente para o aplicativo. O aplicativo não chama diretamente as APIs DMO aplicativo.
-   Aplicativos baseados no Microsoft DirectSound podem usar DMOs de efeito de áudio. Novamente, o aplicativo é protegido das APIs de DMO de nível inferior pelas APIs DirectSound de nível superior.
-   Os aplicativos podem usar DMOs diretamente.

Portanto, ao escrever um DMO, você cria um componente que pode ser usado em uma ampla variedade de aplicativos. Esta documentação contém as seguintes seções:

-   [Sobre DMOs](about-dmos.md)
-   [Usando DMOs](using-dmos.md)
-   [Escrevendo um DMO](writing-a-dmo.md)
-   [Parâmetros de mídia](media-parameters.md)
-   [DMO Referência](dmo-reference.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow](directshow.md)
</dt> </dl>

 

 
