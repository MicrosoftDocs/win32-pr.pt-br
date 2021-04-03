---
title: Tipos de mídia
description: Tipos de mídia
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- SDK do Windows Media Format, tipos de mídia
- ASF (Advanced Systems Format), tipos de mídia
- ASF (formato de sistemas avançados), tipos de mídia
- tipos de mídia, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35005498e8b0625f404e9a54a51cddc65fbfd7bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084123"
---
# <a name="media-types"></a>Tipos de mídia

Os tipos de mídia identificam os diferentes tipos de mídia que podem ser usados pelo SDK do Windows Media Format. Todos os tipos de mídia são valores de GUID que foram atribuídos a constantes no SDK. Os valores de GUID representados pelas constantes listadas nesta seção são listados na seção [identificadores de tipo de mídia](media-type-identifiers.md) desta referência.

A tabela a seguir lista os principais tipos de mídia. Essas constantes definem a classificação de alto nível de mídia digital com suporte no Windows Media Format SDK.



| Tipo principal                | Descrição                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| Vídeo do WMMEDIATYPE \_        | Um fluxo de vídeo.                                                                                         |
| \_Áudio WMMEDIATYPE        | Um fluxo de áudio.                                                                                        |
| \_Script WMMEDIATYPE       | Um fluxo de script.                                                                                        |
| WMMEDIATYPE \_ FileTransfer | Um fluxo que contém arquivos de dados. Os fluxos da Web, que consistem em arquivos HTML, também têm esse tipo principal. |
| \_Imagem WMMEDIATYPE        | Um fluxo de imagem JPEG para um arquivo de áudio ilustrado (como em uma apresentação de slides).                                 |
| \_Texto WMMEDIATYPE         | Um fluxo de texto.                                                                                          |



 

Além dos principais tipos de mídia com suporte explícito, você pode criar seus próprios tipos de dados arbitrários. Para tipos de dados arbitrários personalizados, você deve garantir que o GUID usado não corresponda a um tipo principal existente.

Um fluxo de mídia geralmente terá um subtipo, além de seu tipo principal. As seções a seguir listam os subtipos com suporte.



| Seção                                                        | Descrição                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Subtipos de mídia descompactados](uncompressed-media-subtypes.md) | Descreve os subtipos disponíveis para mídias não compactadas. Esses são os tipos normalmente associados à mídia de entrada ou saída.              |
| [Subtipos de mídia compactados](compressed-media-subtypes.md)     | Descreve os subtipos disponíveis para mídia compactada. Esses são os tipos normalmente associados à mídia em um fluxo dentro de um arquivo ASF. |
| [Formatos de entrada de vídeo](video-input-formats.md)                 | Lista os formatos de vídeo aceitos como entradas para o codec do Windows Media Video 9.                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Identificadores de tipo de mídia**](media-type-identifiers.md)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 




