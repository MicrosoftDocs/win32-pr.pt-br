---
description: Trabalhando com tipos de mídia MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Trabalhando com tipos de mídia MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172466"
---
# <a name="working-with-mft-media-types"></a>Trabalhando com tipos de mídia MFT

Um tipo de mídia é uma maneira de descrever o formato de um fluxo de mídia. No Media Foundation, os tipos de mídia são representados pela interface **IMFMediaType** . Essa interface herda a interface **IMFAttributes** . Os detalhes de um tipo de mídia são especificados como atributos.

Para criar um novo tipo de mídia, chame a função **MFCreateMediaType** . Essa função retorna um ponteiro para a interface **IMFMediaType** . O tipo de mídia inicialmente não tem nenhum atributo.

O SDK do Media Foundation fornece várias funções auxiliares para inicializar tipos de mídia a partir de estruturas de formato. Por exemplo, a função **MFInitMediaTypeFromVideoInfoHeader** Inicializa um tipo de vídeo de uma estrutura **VIDEOINFOHEADER** e a função **MFInitMediaTypeFromWaveFormatEx** Inicializa um tipo de vídeo de uma estrutura **WAVEFORMATEX** ou **WAVEFORMATEXTENSIBLE** .

Os tipos de formato usados pelos codecs geralmente são limitados aos descritos pelas estruturas **VIDEOINFOHEADER** e **WAVEFORMATEX** .

Mais informações sobre como criar e acessar Media Foundation tipos de mídia estão disponíveis na documentação do SDK do Media Foundation.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



