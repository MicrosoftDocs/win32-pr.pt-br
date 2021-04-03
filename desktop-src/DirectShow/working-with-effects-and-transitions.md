---
description: Trabalhando com efeitos e transições
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Trabalhando com efeitos e transições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922917"
---
# <a name="working-with-effects-and-transitions"></a>Trabalhando com efeitos e transições

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Os efeitos modificam um único clipe, faixa ou composição. As transições criam seques de uma faixa ou composições para outra.

Os [serviços de edição do DirectShow](directshow-editing-services.md) usam objetos de transformação do DirectX para suas transições de vídeo e efeitos de vídeo. Para transições de vídeo, use qualquer objeto de transformação DirectX de duas entradas 2D. Para efeitos de vídeo, use qualquer objeto de transformação DirectX de entrada One 2-D. A Microsoft não dá mais suporte ao desenvolvimento de objetos de transformação DirectX de terceiros. No entanto, vários são fornecidos com o DirectShow e outros são fornecidos com o Microsoft Internet Explorer. Para obter mais informações sobre as transições fornecidas com o Internet Explorer, consulte [referência de filtros visuais e transições](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).

Para efeitos de áudio, você pode usar qualquer filtro de efeito de áudio do DirectShow. O DES também fornece um [efeito de envelope de volume](volume-envelope-effect.md) para definir o volume em um roteiro ou um clipe. O DES não oferece suporte a transições de áudio.

Esta seção contém os seguintes tópicos:

-   [Adicionando objetos de efeito e transição](adding-effect-and-transition-objects.md)
-   [Visualização de efeitos e transições](previewing-effects-and-transitions.md)
-   [Enumerando efeitos e transições](enumerating-effects-and-transitions.md)
-   [Definindo propriedades em efeitos e transições](setting-properties-on-effects-and-transitions.md)
-   [Direção da transição](transition-direction.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando os serviços de edição do DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 
