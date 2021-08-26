---
description: Trabalhando com tipos de mídia MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Trabalhando com tipos de mídia MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ead31c4291cf41cff62f4341227bf0ee1ad22d12e96a6c9eff87ff5a3e6faa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886946"
---
# <a name="working-with-mft-media-types"></a>Trabalhando com tipos de mídia MFT

Um tipo de mídia é uma maneira de descrever o formato de um fluxo de mídia. No Media Foundation, os tipos de mídia são representados pela interface **IMFMediaType.** Essa interface herda a interface **IMFAttributes.** Os detalhes de um tipo de mídia são especificados como atributos.

Para criar um novo tipo de mídia, chame a **função MFCreateMediaType.** Essa função retorna um ponteiro para a interface **IMFMediaType.** O tipo de mídia inicialmente não tem atributos.

O Media Foundation SDK fornece várias funções auxiliares para inicializar tipos de mídia de estruturas de formato. Por exemplo, a função **MFInitMediaTypeFromVideoInfoHeader** inicializa um tipo de vídeo de uma estrutura **VIDEOINFOHEADER** e a função **MFInitMediaTypeFromWaveFormatEx** inicializa um tipo de vídeo de uma estrutura **WAVEFORMATEX** ou **WAVEFORMATEXTENSIBLE.**

Os tipos de formato usados pelos codecs geralmente são limitados aos descritos pelas estruturas **VIDEOINFOHEADER** e **WAVEFORMATEX.**

Mais informações sobre como criar e acessar Media Foundation de mídia estão disponíveis na documentação Media Foundation SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com MFTs codec](workingwithcodecmfts.md)
</dt> </dl>

 

 



