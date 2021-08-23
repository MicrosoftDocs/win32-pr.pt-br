---
description: Subobjetos
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Subobjetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf828d0049816c0cbf932b96344b0270c4c9dbfb835a0750736551ff67b319b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633476"
---
# <a name="subobjects"></a>Subobjetos

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Fontes, efeitos e transições têm ponteiros internos para outros objetos COM, chamados *subobjetos*. O subobjeto executa o trabalho real do objeto . O subobjeto de uma origem é o componente que cria os dados de áudio ou vídeo. O subobjeto de um efeito ou transição é o componente que transforma os dados; por exemplo, em um efeito de vídeo, ele cria o efeito visual no fluxo de vídeo.

O tipo de subobjeto depende do tipo de objeto:

-   Origem: qualquer filtro ou filtro de analisador de origem do DirectShow que dá suporte à busca e produz um formato compatível com o DES. Pode ser um formato compactado se existirem filtros DirectShow para decodificá-lo.
-   Efeito: para vídeo, qualquer objeto Microsoft de uma entrada 2D® DirectX® Transform. Para áudio, qualquer filtro de efeito de áudio directShow.
-   Transição: para vídeo, qualquer objeto de Transformação DirectX de duas entradas 2D. O áudio não dá suporte a transições.

Grupos, composições e faixas não têm subobjetos.

O aplicativo não configura diretamente o ponteiro do subobjeto. Para efeitos e transições, o aplicativo chama o método [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) para especificar o GUID do subobjeto. Para objetos de origem, um aplicativo normalmente chama [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) para especificar o nome de um arquivo de origem. No entanto, **o método SetSubObjectGUID** também pode ser usado para objetos de origem, para especificar o CLSID (identificador de classe) de um filtro.

Para obter mais informações, consulte [Trabalhando com fontes e](working-with-sources.md) trabalhando com efeitos e [transições.](working-with-effects-and-transitions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral dos componentes da linha do tempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



