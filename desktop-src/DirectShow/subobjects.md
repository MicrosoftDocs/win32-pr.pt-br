---
description: Subobjetos
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Subobjetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829371"
---
# <a name="subobjects"></a>Subobjetos

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Fontes, efeitos e transições têm ponteiros internos para outros objetos COM, chamados de *subobjetos*. O subobjeto executa o trabalho real do objeto. O subobjeto de uma origem é o componente que cria os dados de vídeo ou áudio. O subobjeto de um efeito ou transição é o componente que transforma os dados; por exemplo, em um efeito de vídeo, ele cria o efeito visual no fluxo de vídeo.

O tipo de subobjeto depende do tipo de objeto:

-   Fonte: qualquer filtro de origem ou filtro do analisador do DirectShow que ofereça suporte à busca e produza um formato compatível com o DES. Ele pode ser um formato compactado se houver filtros do DirectShow para decodificá-lo.
-   Efeito: para vídeo, qualquer objeto de transformação One-D da Microsoft® DirectX® Transform. Para áudio, qualquer filtro de efeito de áudio do DirectShow.
-   Transição: para vídeo, qualquer objeto de transformação DirectX de duas entradas 2-D. O áudio não oferece suporte a transições.

Grupos, composições e faixas não têm subobjetos.

O aplicativo não define diretamente o ponteiro do subobjeto. Para efeitos e transições, o aplicativo chama o método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) para especificar o GUID do subobjeto. Para objetos de origem, um aplicativo normalmente chama o [**IAMTimelineSrc:: Setmedianame**](iamtimelinesrc-setmedianame.md) para especificar o nome de um arquivo de origem. No entanto, o método **SetSubObjectGUID** também pode ser usado para objetos de origem, para especificar o identificador de classe (CLSID) de um filtro.

Para obter mais informações, consulte [trabalhando com fontes](working-with-sources.md) e [trabalhando com efeitos e transições](working-with-effects-and-transitions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral dos componentes da linha do tempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



