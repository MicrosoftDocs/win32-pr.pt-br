---
title: Tipos de mídia para Windows SDK de formato de mídia
description: Saiba mais sobre os tipos de mídia que podem ser usados pelo SDK Windows Formato de Mídia. Os tipos de mídia são valores GUID atribuídos a constantes no SDK.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows SDK de Formato de Mídia, tipos de mídia
- ASF (Advanced Systems Format), tipos de mídia
- ASF (Formato de Sistemas Avançados), tipos de mídia
- tipos de mídia, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84974391a7e044367fd298598181d43447cfac4bec1829b9e5ddb0b90ae27ea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027484"
---
# <a name="media-types-for-windows-media-format-sdk"></a>Tipos de mídia para Windows SDK de formato de mídia

Os tipos de mídia identificam os diferentes tipos de mídia que podem ser usados pelo SDK Windows Formato de Mídia. Todos os tipos de mídia são valores GUID que foram atribuídos a constantes no SDK. Os valores guid representados pelas constantes listadas nesta seção são listados na seção [Identificadores](media-type-identifiers.md) de Tipo de Mídia desta referência.

A tabela a seguir lista os principais tipos de mídia. Essas constantes definem a classificação de alto nível de mídia digital com suporte pelo SDK Windows Formato de Mídia.



| Tipo principal                | Descrição                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| Vídeo \_ wmmediatype        | Um fluxo de vídeo.                                                                                         |
| Áudio \_ WMMEDIATYPE        | Um fluxo de áudio.                                                                                        |
| WMMEDIATYPE \_ Script       | Um fluxo de script.                                                                                        |
| WMMEDIATYPE \_ FileTransfer | Um fluxo que contém arquivos de dados. Os fluxos da Web, que consistem em arquivos HTML, também têm esse tipo principal. |
| Imagem \_ WMMEDIATYPE        | Um fluxo de imagem JPEG para um arquivo de áudio ilustrado (como em uma apresentação de slides).                                 |
| Texto \_ WMMEDIATYPE         | Um fluxo de texto.                                                                                          |



 

Além dos principais tipos de mídia com suporte explícito, você pode criar seus próprios tipos de dados arbitrários. Para tipos de dados arbitrários personalizados, você deve garantir que o GUID usado não corresponderá a um tipo principal existente.

Um fluxo de mídia geralmente terá um subtipo além de seu tipo principal. As seções a seguir listam os subtipos com suporte.



| Seção                                                        | Descrição                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Subtipos de mídia descompactados](uncompressed-media-subtypes.md) | Descreve os subtipos disponíveis para mídia descompactada. Esses são os tipos normalmente associados à mídia de entrada ou saída.              |
| [Subtipos de mídia compactado](compressed-media-subtypes.md)     | Descreve os subtipos disponíveis para mídia compactada. Esses são os tipos normalmente associados à mídia em um fluxo dentro de um arquivo ASF. |
| [Formatos de entrada de vídeo](video-input-formats.md)                 | Lista os formatos de vídeo aceitos como entradas para o codec Windows Media Video 9.                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Identificadores de tipo de mídia**](media-type-identifiers.md)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 




