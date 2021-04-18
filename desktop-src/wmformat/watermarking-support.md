---
title: Suporte à marca d' água
description: Suporte à marca d' água
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- SDK do Windows Media Format, suporte a marca d' água
- SDK do Windows Media Format, marca d' água digital
- Formato de sistema avançado (ASF), suporte à marca d' água
- ASF (formato de sistemas avançados), suporte à marca d' água
- ASF (Advanced Systems Format), marca d' água digital
- ASF (formato de sistemas avançados), marca d' água digital
- SDK do Windows Media Format, DMO
- ASF (Advanced Systems Format), DMO
- ASF (formato de sistemas avançados), DMO
- SDK do Windows Media Format, interface IWMWatermarkInfo
- Formato de sistema avançado (ASF), interface IWMWatermarkInfo
- ASF (formato de sistemas avançados), interface IWMWatermarkInfo
- marca d' água, sobre
- marca d' água digital
- Objeto de mídia do DirectX (DMO), sobre
- DMO (objeto de mídia DirectX), sobre
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105813219"
---
# <a name="watermarking-support"></a>Suporte à marca d' água

A marca d' água digital é uma maneira de inserir direitos autorais ou outras informações nos dados de um fluxo de mídia. As técnicas para a marca d' água variam muito de uma solução para a próxima. A forma mais simples de marca d' água é simplesmente adicionar uma imagem de identificação a cada quadro de um fluxo de vídeo. Estações de televisão frequentemente usam essa técnica para inserir um logotipo semitransparente em um canto inferior de sua difusão. Formas mais sofisticadas de marca d' água digital são imperceptívels para o usuário assistir ou ouvir o conteúdo.

O SDK do Windows Media Format dá suporte ao uso de [*DMOs*](wmformat-glossary.md)de marca d' água digital. Na prática, um sistema de marca d' água é muito semelhante a um codec: ele usa amostras de mídia, executa algoritmos nos dados e gera os exemplos alterados. Quando um sistema de marca d' água é especificado para um fluxo, o objeto do gravador inclui o DMO em seu processamento de exemplos de entrada.

Você deve especificar informações de configuração de marca d' água ao configurar um fluxo para a marca d' água. Os valores de configuração serão diferentes dependendo da marca d' água do DMO. O DMO que você usa deve vir com instruções que descrevem os valores de configuração que ele suporta.

Para obter informações sobre as configurações usadas para especificar um sistema de marca d' água, consulte [ **IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)

Você pode programar seu aplicativo para enumerar o DMOs de marca d' água instalado no computador cliente. Para obter mais informações, consulte a interface [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de gravação de arquivo**](file-writing-features.md)
</dt> </dl>

 

 




