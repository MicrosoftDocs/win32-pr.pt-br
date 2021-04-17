---
description: Processadores de sinais digitais
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Processadores de sinais digitais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0961554d9c9902e68f74c6b2b57662b23846614f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105763487"
---
# <a name="digital-signal-processors"></a>Processadores de sinais digitais

Esta seção descreve os objetos do processador de sinais digitais (DSP) fornecidos pelo Windows.

A Microsoft usa o termo *processador de sinal digital* para designar um conjunto de objetos com que executam transformações em dados de vídeo e áudio não compactados. Os DSPs descritos neste SDK transformam áudio e vídeo em uma variedade de formatos descompactados.

Os DSPs podem ser usados por si próprios ou em combinação com codecs de áudio e vídeo. Com exceção do DSP de captura de voz, cada DSP listado aqui implementa duas interfaces separadas, mas semelhantes.



| Interface                              | Descrição                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatível com Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatível com o DirectShow.                 |



 

Você pode configurar os DSPs usando a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir propriedades. Alguns dos DSPs têm interfaces adicionais que definem propriedades. Para usar essas interfaces, chame o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de qualquer outra interface do DSP. O tópico de referência para cada DSP lista as propriedades, interfaces e outros recursos com suporte.

Esta seção contém os seguintes tópicos.



| DSP                                                      | Descrição                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [DSP de reamostragem de áudio](audioresampler.md)                | Converte a taxa de amostragem de um fluxo de áudio.       |
| [DSP de transformação de controle de cores](colorcontroltransform.md) | Ajusta as características de cor de um fluxo de vídeo. |
| [DSP de conversor de cores](colorconverter.md)                | Converte um fluxo de vídeo entre formatos de cor.       |
| [Conversor de taxa de quadros DSP](framerateconverter.md)       | Altera a taxa de quadros de um fluxo de vídeo.            |
| [DSP de redimensionador de vídeo](videoresizer.md)                    | Redimensiona um fluxo de vídeo.                              |
| [DSP de captura de voz](voicecapturedmo.md)                 | Encapsula vários DSPs relacionados à captura de voz.  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação do Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
