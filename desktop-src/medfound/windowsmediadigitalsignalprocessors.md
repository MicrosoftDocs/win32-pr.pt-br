---
description: Processadores de sinal digital
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Processadores de sinal digital
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f5c9aa0ee3c4cc2a8c7f725b3a8444f4852c8c5b52ee3713b533ec435f4a3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100938"
---
# <a name="digital-signal-processors"></a>Processadores de sinal digital

Esta seção descreve os objetos DSP (processador de sinal digital) fornecidos pelo Windows.

A Microsoft usa o termo *processador de sinal digital* para designar um conjunto de objetos COM que executam transformações em dados de áudio e vídeo descompactados. Os DSPs descritos neste SDK transformam áudio e vídeo em uma variedade de formatos descompactados.

Os DSPs podem ser usados por si mesmos ou em combinação com codecs de áudio e vídeo. Com exceção do DSP de Captura de Voz, cada DSP listado aqui implementa duas interfaces separadas, mas semelhantes.



| Interface                              | Descrição                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatível com Microsoft Media Foundation. |
| [**Imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatível com DirectShow.                 |



 

Você pode configurar os DSPs usando a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir propriedades. Alguns dos DSPs têm interfaces adicionais que configuram propriedades. Para usar essas interfaces, chame o [**método QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de qualquer outra interface do DSP. O tópico de referência para cada DSP lista as propriedades, as interfaces e outros recursos com suporte.

Esta seção contém os seguintes tópicos.



| Dsp                                                      | Descrição                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [Audio Resampler DSP](audioresampler.md)                | Converte a taxa de amostragem de um fluxo de áudio.       |
| [DSP (Transformação Controle de Cores)](colorcontroltransform.md) | Ajusta as características de cor de um fluxo de vídeo. |
| [DSP do Conversor de Cores](colorconverter.md)                | Converte um fluxo de vídeo entre formatos de cor.       |
| [DSP do Conversor de Taxa de Quadros](framerateconverter.md)       | Altera a taxa de quadros de um fluxo de vídeo.            |
| [DSP do Resizer de Vídeo](videoresizer.md)                    | Resize um fluxo de vídeo.                              |
| [DSP de Captura de Voz](voicecapturedmo.md)                 | Encapsula vários DSPs relacionados à captura de voz.  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação do Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
