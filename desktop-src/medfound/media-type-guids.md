---
description: Principais tipos de mídia
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Principais tipos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56553ac635f0e767e43e057b2a468027dcefb730
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549571"
---
# <a name="major-media-types"></a>Principais tipos de mídia

Em um tipo de mídia, *o tipo principal* descreve a categoria geral dos dados, como áudio ou vídeo. O *subtipo*, se presente, refina ainda mais o tipo principal. Por exemplo, se o tipo principal for vídeo, o subtipo poderá ser um vídeo RGB de 32 bits. Os subtipos também distinguem formatos codificados, como vídeo H.264, de formatos descompactados.

O tipo principal e o subtipo são identificados por GUIDs e armazenados nos seguintes atributos:



| Atributo                                             | Descrição |
|-------------------------------------------------------|-------------|
| [MF \_ MT \_ MAJOR \_ TYPE](mf-mt-major-type-attribute.md) | Tipo principal. |
| [SUBTIPO \_ MF MT \_](mf-mt-subtype-attribute.md)        | Subtipo.    |



 

Os seguintes tipos principais são definidos.



| Tipo principal                    | Description                                                                                                                                                | Subtipos                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **Áudio MFMediaType \_**        | Áudio.                                                                                                                                                     | [GUIDs de subtipo de áudio.](audio-subtype-guids.md)      |
| **Binário MFMediaType \_**       | Fluxo binário.                                                                                                                                             | Nenhum.                                                |
| **Arquivo \_ MFMediaTypeTransfer** | Um fluxo que contém arquivos de dados.                                                                                                                         | Nenhum.                                                |
| **\_HTML MFMediaType**         | Fluxo de HTML.                                                                                                                                               | Nenhum.                                                |
| **\_Imagem MFMediaType**        | Fluxo de imagem ainda.                                                                                                                                        | [GUIDs e CLSIDs do WIC](../wic/-wic-guids-clsids.md).       |
| **Metadados do MFMediaType \_**        | Fluxo de metadados.                                                                                                                                        | Nenhum.       |
| **MFMediaType \_ protegido**    | Mídia protegida.                                                                                                                                           | O subtipo especifica o esquema de proteção de conteúdo. |
| **Percepção de MFMediaType \_**   | Transmite de um sensor de câmera ou unidade de processamento por razões e compreende dados brutos de vídeo e fornece compreensão do ambiente ou dos seres humanos. | Nenhum.                                                |
| **Sami de MFMediaType \_**         | Legendas de SAMI (intercâmbio de mídia acessível) sincronizadas.                                                                                                 | Nenhum.                                                |
| **\_Script MFMediaType**       | Fluxo de script.                                                                                                                                             | Nenhum.                                                |
| **Fluxo de MFMediaType \_**       | Fluxo multiplexado ou fluxo elementar.                                                                                                                   | [GUIDs de subtipo de fluxo](stream-subtype-guids.md)     |
| **Vídeo MFMediaType \_**        | Vídeo.                                                                                                                                                     | [GUIDs de subtipo de vídeo.](video-subtype-guids.md)      |



 

Componentes de terceiros podem definir novos tipos principais e novos subtipos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 
