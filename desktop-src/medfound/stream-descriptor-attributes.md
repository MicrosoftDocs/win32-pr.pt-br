---
description: Atributos do descritor de fluxo
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Atributos do descritor de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647735"
---
# <a name="stream-descriptor-attributes"></a>Atributos do descritor de fluxo

## <a name="common-stream-descriptor-attributes"></a>Atributos comuns de descritor de fluxo

Os atributos a seguir se aplicam aos descritores de fluxo.



| Atributo                                                   | Descrição                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**\_linguagem SD \_ MF**](mf-sd-language-attribute.md)        | Especifica o idioma de um fluxo.                                                  |
| [MF \_ SD \_ mutuamente \_ exclusivo](mf-sd-mutually-exclusive.md) | Especifica se um fluxo é mutuamente exclusivo com outros fluxos do mesmo tipo. |
| [**MF \_ SD \_ protegido**](mf-sd-protected-attribute.md)      | Especifica se um fluxo contém conteúdo protegido.                                |
| [\_nome do \_ fluxo \_ SD MF](mf-sd-stream-name.md)               | Contém o nome de um fluxo.                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a>ASF-Specific atributos de descritor de fluxo

Os atributos a seguir se aplicam a descritores de fluxo para arquivos ASF (Advanced Systems Format).



| Atributo                                                                                                                | Descrição                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ média \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | Especifica o tamanho médio do buffer necessário para um fluxo em um arquivo ASF, em bytes.            |
| [**\_taxa de \_ \_ \_ bits média de \_ dados \_ do MF SD EXTSTRMPROP**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | Especifica a taxa média de bits de dados de um fluxo em um arquivo ASF, em bits por segundo.        |
| [**índice de ID de idioma do MF \_ SD \_ ASF \_ EXTSTRMPROP \_ \_ \_**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | Especifica o idioma usado por um fluxo em um arquivo ASF.                                    |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Max \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | Especifica o tamanho máximo de buffer necessário para um fluxo em um arquivo ASF, em bytes.            |
| [**\_taxa de \_ \_ \_ bits máxima de \_ dados EXTSTRMPROP \_ MF SD**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | Especifica a taxa máxima de bits de dados de um fluxo em um arquivo ASF, em bits por segundo         |
| [**\_modelo de \_ \_ conformidade do dispositivo de metadados do ASF \_ SD \_ MF \_**](mf-sd-asf-metadata-device-conformance-template-attribute.md) | Especifica o modelo de conformidade do dispositivo para um fluxo em um arquivo ASF, em bits por segundo. |
| [**\_taxa de \_ \_ bits STREAMBITRATES do ASF SD \_**](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | Especifica a taxa média de bits de um fluxo em um arquivo ASF, em bits por segundo.             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a>Atributos do descritor de fluxo de origem de mídia SAMI

O atributo a seguir aplica-se ao descritor de fluxo para a origem de mídia SAMI.



| Atributo                                                       | Descrição                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**\_linguagem de \_ Sami \_ SD MF**](mf-sd-sami-language-attribute.md) | Contém o nome do idioma de intercâmbio de mídia acessível (SAMI) que é definido para o fluxo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



