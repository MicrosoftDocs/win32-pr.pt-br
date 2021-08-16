---
title: Trabalhando com High-Resolution áudio PCM
description: Trabalhando com High-Resolution áudio PCM
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- ASF (Advanced Systems Format), áudio PCM de alta resolução
- ASF (Formato de Sistemas Avançados), áudio PCM de alta resolução
- perfis, áudio PCM de alta resolução
- codecs, áudio PCM de alta resolução
- ASF (Advanced Systems Format), áudio PCM
- ASF (formato de sistemas avançados), áudio PCM
- perfis, áudio PCM
- codecs, áudio PCM
- áudio PCM de alta resolução
- Áudio pcm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a76cfb8397cacd6d39f62ea3594c8be655f4543e0b48b60cafbf15b9783c7fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194851"
---
# <a name="working-with-high-resolution-pcm-audio"></a>Trabalhando com High-Resolution áudio PCM

Alguns dos formatos de entrada para o codec Professional do Windows Media Audio 9 e o codec sem perda Windows Media Audio 9 são formatos PCM de alta resolução. Esses são formatos PCM que têm mais de dois canais ou mais de 16 bits por exemplo (áudio com mais de dois canais também é chamado de áudio multicanal).

Esses formatos são configurados usando uma extensão estruturada da estrutura [**WAVEFORMATEX,**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) chamada [**WAVEFORMATEXTENSIBLE.**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) A **estrutura WAVEFORMATEXTENSIBLE** inclui informações sobre os canais incluídos no áudio. Essa estrutura é necessária ao usar áudio PCM de alta resolução, porque algumas APIs Windows não aceitarão estruturas **WAVEFORMATEX** que contêm valores de alta resolução.

Formatos PCM de alta resolução têm 22 bytes de dados estendidos, que são especificados no membro **cbSize** da **estrutura WAVEFORMATEX.** Os formatos de Windows mídia de alta resolução não usam a estrutura **WAVEFORMATEXTENSIBLE,** mas têm dados estendidos anexados à estrutura **WAVEFORMATEX.**

Os codecs de áudio Windows Media só suportam a decodificação para formatos PCM de alta resolução quando o aplicativo está em execução no Windows XP ou posterior. Nas versões anteriores do Microsoft Windows, os codecs decodificam para um formato com um máximo de 16 bits por exemplo e 2 canais. Além disso, você deve especificar que deseja que o codec decodificar para PCM de alta definição definindo a configuração de saída g \_ wszEnableDiscreteOutput como **TRUE** usando o [**método IWMReaderAdvanced2::SetOutputSetting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) Depois de fazer essa chamada, as saídas enumeradas pelo leitor incluirão formatos de alta definição.

O áudio multicanal requer mais configuração. Para obter mais informações, consulte [Lendo áudio multicanal.](reading-multichannel-audio.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> </dl>

 

 