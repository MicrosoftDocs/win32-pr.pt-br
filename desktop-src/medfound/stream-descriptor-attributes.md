---
description: Atributos do descritor de fluxo
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Atributos do descritor de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5db29ef0076415ff07e9ed25f7e6ca3e0588ec25257802fe0c7829ab3178c935
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953226"
---
# <a name="stream-descriptor-attributes"></a>Atributos do descritor de fluxo

## <a name="common-stream-descriptor-attributes"></a>Atributos comuns do descritor de fluxo

Os atributos a seguir se aplicam a descritores de fluxo.



| Atributo                                                   | Descrição                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**LINGUAGEM \_ SD do MF \_**](mf-sd-language-attribute.md)        | Especifica o idioma de um fluxo.                                                  |
| [MF \_ SD \_ MUTUAMENTE \_ EXCLUSIVO](mf-sd-mutually-exclusive.md) | Especifica se um fluxo é mutuamente exclusivo com outros fluxos do mesmo tipo. |
| [**MF \_ SD \_ PROTEGIDO**](mf-sd-protected-attribute.md)      | Especifica se um fluxo contém conteúdo protegido.                                |
| [MF \_ SD \_ STREAM \_ NAME](mf-sd-stream-name.md)               | Contém o nome de um fluxo.                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a>ASF-Specific atributos do descritor de fluxo

Os atributos a seguir se aplicam a descritores de fluxo para arquivos ASF (Advanced Systems Format).



| Atributo                                                                                                                | Descrição                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | Especifica o tamanho médio do buffer necessário para um fluxo em um arquivo ASF, em bytes.            |
| [**TAXA DE \_ BITS DE DADOS MF SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ \_**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | Especifica a taxa média de bits de dados de um fluxo em um arquivo ASF, em bits por segundo.        |
| [**ÍNDICE \_ DE ID DA LINGUAGEM \_ \_ EXTSTRMPROP \_ \_ \_ DO MF SD**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | Especifica o idioma usado por um fluxo em um arquivo ASF.                                    |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | Especifica o tamanho máximo do buffer necessário para um fluxo em um arquivo ASF, em bytes.            |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | Especifica a taxa máxima de bits de dados de um fluxo em um arquivo ASF, em bits por segundo         |
| [**MODELO DE CONFORMIDADE DO DISPOSITIVO \_ MF SD \_ ASF \_ METADATA \_ \_ \_**](mf-sd-asf-metadata-device-conformance-template-attribute.md) | Especifica o modelo de conformidade do dispositivo para um fluxo em um arquivo ASF, em bits por segundo. |
| [**TAXA DE \_ BITS \_ \_ STREAMBITRATES DO ASF SD \_**](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | Especifica a taxa média de bits de um fluxo em um arquivo ASF, em bits por segundo.             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a>Atributos do descritor de fluxo de origem de mídia SAMI

O atributo a seguir se aplica ao descritor de fluxo para a fonte de mídia SAMI.



| Atributo                                                       | Descrição                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**LINGUAGEM \_ SAMI do MF SD \_ \_**](mf-sd-sami-language-attribute.md) | Contém o nome de idioma SAMI (Synchronized Accessible Media Interchange) definido para o fluxo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 



