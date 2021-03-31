---
title: Trabalhando com High-Resolution áudio PCM
description: Trabalhando com High-Resolution áudio PCM
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- ASF (Advanced Systems Format), áudio PCM de alta resolução
- ASF (formato de sistemas avançados), áudio PCM de alta resolução
- perfis, áudio PCM de alta resolução
- codecs, áudio PCM de alta resolução
- ASF (Advanced Systems Format), áudio PCM
- ASF (formato de sistemas avançados), áudio PCM
- perfis, áudio PCM
- codecs, áudio PCM
- áudio PCM de alta resolução
- Áudio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917419"
---
# <a name="working-with-high-resolution-pcm-audio"></a>Trabalhando com High-Resolution áudio PCM

Alguns dos formatos de entrada para o codec do Windows Media Audio 9 Professional e o codec do Windows Media Audio 9 sem perdas são formatos PCM de alta resolução. Esses são formatos PCM que têm mais de dois canais, ou mais de 16 bits por amostra (áudio com mais de dois canais também é chamado de áudio de multicanal).

Esses formatos são configurados usando uma extensão estruturada da estrutura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) , chamada [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)). A estrutura **WAVEFORMATEXTENSIBLE** inclui informações sobre os canais incluídos no áudio. Essa estrutura é necessária ao usar áudio PCM de alta resolução, pois algumas APIs do Windows não aceitarão estruturas **WAVEFORMATEX** que contenham valores de alta resolução.

Os formatos PCM de alta resolução têm 22 bytes de dados estendidos, que é especificado no membro **cbSize** da estrutura **WAVEFORMATEX** . Os formatos de áudio do Windows Media de alta resolução não usam a estrutura **WAVEFORMATEXTENSIBLE** , mas têm dados estendidos anexados à estrutura **WAVEFORMATEX** .

Os codecs de áudio do Windows Media só dão suporte à decodificação de formatos PCM de alta resolução quando o aplicativo está em execução no Windows XP ou posterior. Nas versões anteriores do Microsoft Windows, os codecs decodificam para um formato com um máximo de 16 bits por amostra e 2 canais. Além disso, você deve especificar que deseja que o codec decodifique para o PCM de alta definição definindo a \_ configuração de saída g wszEnableDiscreteOutput como **true** usando o método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) . Depois de fazer essa chamada, as saídas enumeradas pelo leitor incluirão formatos de alta definição.

O áudio de multicanal requer mais configuração. Para obter mais informações, consulte [lendo áudio multicanal](reading-multichannel-audio.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> </dl>

 

 