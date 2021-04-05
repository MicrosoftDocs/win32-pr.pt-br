---
title: Interpolação de quadros
description: Interpolação de quadros
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- SDK do Windows Media Format, interpolação de quadros
- codecs, interpolação de quadros
- interpolação de quadros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007114"
---
# <a name="frame-interpolation"></a>Interpolação de quadros

A interpolação de quadros é o processo de criação de quadros de vídeo intermediários com base nos dados em dois quadros consecutivos de vídeo codificado. Na verdade, a interpolação de quadros aumenta a [*taxa de quadros*](wmformat-glossary.md) do vídeo codificado no momento da decodificação. Você pode usar a interpolação de quadro para melhorar a suavidade de reprodução de fluxos de vídeo com taxas de quadros baixas.

Como esse é um recurso de decodificação, ele não envolve nenhuma opção de codificação especial e não adiciona sobrecarga ao conteúdo. A interpolação do quadro é especificada como uma configuração de saída no objeto leitor.

Somente o codec do Windows Media Video 9 dá suporte à interpolação de quadros.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos do codec**](codec-features.md)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**Configurações de saída**](output-settings.md)
</dt> </dl>

 

 




