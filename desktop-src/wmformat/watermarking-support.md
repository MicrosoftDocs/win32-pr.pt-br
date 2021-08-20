---
title: Suporte à marca d'água
description: Suporte à marca d'água
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows SDK de Formato de Mídia, suporte a marca d'água
- Windows SDK de formato de mídia, marca d'água digital
- AsF (Advanced Systems Format), suporte à marca d'água
- ASF (Formato de Sistemas Avançados), suporte à marca d'água
- ASF (Advanced Systems Format), marca d'água digital
- ASF (Formato de Sistemas Avançados), marca d'água digital
- Windows SDK de formato de mídia, DMO
- ASF (Advanced Systems Format), DMO
- ASF (formato de sistemas avançados), DMO
- Windows SDK de Formato de Mídia, interface IWMWatermarkInfo
- AsF (Advanced Systems Format), interface IWMWatermarkInfo
- ASF (Formato de Sistemas Avançados), interface IWMWatermarkInfo
- marca d'água,sobre
- marca d'água digital
- DirectX Media Object (DMO),sobre
- DMO (Objeto de Mídia DirectX),sobre
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78610c95d041390f819c24a11ccbf393bd62d19037e655e2d1c53b458e0a664b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653429"
---
# <a name="watermarking-support"></a>Suporte à marca d'água

A marca d'água digital é uma maneira de inserir direitos autorais ou outras informações nos dados de um fluxo de mídia. As técnicas de marca d'água variam muito de uma solução para a próxima. A forma mais simples de marca d'água é simplesmente adicionar uma imagem de identificação a cada quadro de um fluxo de vídeo. As estações de tv frequentemente usam essa técnica para inserir um logotipo semi transparente em um canto inferior de sua difusão. Formas mais sofisticadas de marca d'água digital são imperceptíveis para o usuário que está assistindo ou escutando o conteúdo.

O Windows SDK de Formato de Mídia do Windows dá suporte ao uso de DMOs de marca [*d'água*](wmformat-glossary.md)digital. Na prática, um sistema de marca-d'água é muito semelhante a um codec: ele recebe exemplos de mídia, executa algoritmos nos dados e saída dos exemplos alterados. Quando um sistema de marca-d'água é especificado para um fluxo, o objeto writer inclui o DMO em seu processamento de exemplos de entrada.

Você deve especificar informações de configuração de marca d'água ao configurar um fluxo para marca-d'água. Os valores de configuração serão diferentes dependendo da marca d'água DMO. O DMO que você usa deve vir com instruções que descrevem os valores de configuração aos qual ele dá suporte.

Para obter informações sobre as configurações usadas para especificar um sistema de marca-d'água, consulte [ **IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)

Você pode programar seu aplicativo para enumerar os DMOs de marca d'água instalados no computador cliente. Para obter mais informações, consulte a interface [**IWMWatermarkInfo.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de escrita de arquivo**](file-writing-features.md)
</dt> </dl>

 

 




