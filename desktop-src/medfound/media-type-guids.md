---
description: Tipos de mídia principais
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Tipos de mídia principais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec660dcb86cfd1da5a80bef106ee8ddd17cf1e89899fea6b824fba5ab9be04e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715296"
---
# <a name="major-media-types"></a>Tipos de mídia principais

Em um tipo de mídia, o *tipo principal* descreve a categoria geral dos dados, como áudio ou vídeo. O *subtipo*, se presente, refinará o tipo principal. Por exemplo, se o tipo principal for vídeo, o subtipo poderá ser um vídeo RGB de 32 bits. Os subtipos também distinguem os formatos codificados, como o vídeo H. 264, de formatos descompactados.

O tipo principal e o subtipo são identificados por GUIDs e armazenados nos seguintes atributos:



| Atributo                                             | Descrição |
|-------------------------------------------------------|-------------|
| [\_ \_ tipo principal MF \_ MT](mf-mt-major-type-attribute.md) | Tipo principal. |
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)        | Subtipo.    |



 

Os seguintes tipos principais são definidos.



| Tipo principal                    | Descrição                                                                                                                                                | Subtipos                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **\_Áudio MFMediaType**        | Sonoro.                                                                                                                                                     | [GUIDs de subtipo de áudio](audio-subtype-guids.md).      |
| **MFMediaType \_ binário**       | Fluxo binário.                                                                                                                                             | Nenhum.                                                |
| **MFMediaType \_ FileTransfer** | Um fluxo que contém arquivos de dados.                                                                                                                         | Nenhum.                                                |
| **\_HTML MFMediaType**         | Fluxo de HTML.                                                                                                                                               | Nenhum.                                                |
| **\_Imagem MFMediaType**        | Fluxo de imagem ainda.                                                                                                                                        | [GUIDs e CLSIDs do WIC](../wic/-wic-guids-clsids.md).       |
| **Metadados do MFMediaType \_**        | Fluxo de metadados.                                                                                                                                        | Nenhum.       |
| **MFMediaType \_ protegido**    | Mídia protegida.                                                                                                                                           | O subtipo especifica o esquema de proteção de conteúdo. |
| **Percepção de MFMediaType \_**   | Fluxos de um sensor de câmera ou unidade de processamento que os motivos e entenda os dados brutos de vídeo e fornece a compreensão do ambiente ou dos seres humanos. | Nenhum.                                                |
| **Sami de MFMediaType \_**         | Legendas de SAMI (intercâmbio de mídia acessível) sincronizadas.                                                                                                 | Nenhum.                                                |
| **\_Script MFMediaType**       | Fluxo de script.                                                                                                                                             | Nenhum.                                                |
| **Fluxo de MFMediaType \_**       | Fluxo multiplexado ou fluxo elementar.                                                                                                                   | [GUIDs de subtipo de fluxo](stream-subtype-guids.md)     |
| **Vídeo do MFMediaType \_**        | Vídeo.                                                                                                                                                     | [GUIDs de subtipo de vídeo](video-subtype-guids.md).      |



 

Os componentes de terceiros podem definir novos tipos principais e novos subtipos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 
