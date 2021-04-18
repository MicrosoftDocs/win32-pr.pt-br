---
description: Objetos de mídia do DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Objetos de mídia do DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105778484"
---
# <a name="directx-media-objects"></a>Objetos de mídia do DirectX

> [!Note]  
> DMOs foram substituídas por [Media Foundation transformações](/windows/desktop/medfound/media-foundation-transforms) (MFTs). As interfaces DMO ainda têm suporte. No entanto, se você estiver escrevendo um codec personalizado ou um plug-in de processamento de áudio/vídeo, considere implementá-lo como um MFT.

 

Os DMOs (objetos de mídia do DirectX) são componentes de streaming de dados baseados em COM. Em alguns aspectos, DMOs são semelhantes aos filtros do Microsoft DirectShow. Como os filtros do DirectShow, DMOs pegar dados de entrada e usá-los para produzir dados de saída. No entanto, as APIs (interfaces de programação de aplicativo) para DMOs são muito mais simples do que as APIs correspondentes para o DirectShow. Como resultado, DMOs são mais fáceis de criar, testar e usar. DMOs pode ser usado em muitos cenários:

-   Aplicativos baseados no DirectShow podem usar o DMOs por meio de um filtro do DirectShow chamado de filtro de [invólucro do DMO](dmo-wrapper-filter.md) . A distinção entre filtros e DMOs é transparente para o aplicativo. O aplicativo não chama diretamente as APIs de DMO.
-   Os aplicativos baseados no Microsoft DirectSound podem usar o efeito de áudio DMOs. Novamente, o aplicativo é blindado das APIs de nível inferior de DMO pelas APIs do DirectSound de nível superior.
-   Os aplicativos podem usar o DMOs diretamente.

Assim, escrevendo um DMO, você cria um componente que pode ser usado em uma ampla variedade de aplicativos. Esta documentação contém as seguintes seções:

-   [Sobre o DMOs](about-dmos.md)
-   [Usando DMOs](using-dmos.md)
-   [Escrevendo um DMO](writing-a-dmo.md)
-   [Parâmetros de mídia](media-parameters.md)
-   [Referência de DMO](dmo-reference.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow](directshow.md)
</dt> </dl>

 

 
