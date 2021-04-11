---
title: Modelos de conformidade do dispositivo
description: Modelos de conformidade do dispositivo
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- SDK do Windows Media Format, modelos de conformidade do dispositivo
- codecs, modelos de conformidade do dispositivo
- modelos de conformidade do dispositivo, sobre
- modelos, modelos de conformidade do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eccb88b372f9e0eb463d88db83d70102408a7a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292771"
---
# <a name="device-conformance-templates"></a>Modelos de conformidade do dispositivo

Os codecs do Windows Media 9 Series dão suporte a modelos de conformidade do dispositivo, que são definidos como intervalos de definições de configuração de fluxo e algoritmos de codec. Cada modelo define os intervalos de valores apropriados para determinados dispositivos.

No passado, os fabricantes de hardware que tornaram os dispositivos capazes de reproduzir arquivos ASF estavam funcionando para seus próprios padrões. Isso resultou na ampla variedade de recursos em dispositivos semelhantes que continuam hoje.

Com os modelos de conformidade do dispositivo, os codecs do Windows Media estabelecem um aterramento comum para dispositivos semelhantes. Os fabricantes de hardware podem declarar a quais modelos seus dispositivos estão em conformidade, permitindo que os criadores de conteúdo direcionem com mais confiança seus arquivos para a leitura de dispositivos. Também é mais fácil para os aplicativos de Player determinarem se um arquivo é inadequado para o dispositivo antes de tentar reproduzi-lo.

Um modelo de conformidade do dispositivo é identificado por uma cadeia de caracteres, que é armazenada como um atributo de metadados associado ao fluxo ao qual o modelo se aplica. Para obter uma lista dos modelos e suas cadeias de caracteres e parâmetros, consulte [parâmetros de modelo de conformidade do dispositivo](device-conformance-template-parameters.md).

Os modelos de conformidade do dispositivo têm suporte para todos os codecs do Windows Media 9 Series e posteriores, exceto o codec de tela do Windows Media Video 9 e o codec Windows Media Audio 9 Lossless.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos do codec**](codec-features.md)
</dt> <dt>

[**Trabalhando com modelos de conformidade do dispositivo**](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




