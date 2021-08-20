---
title: Usar o telecine inverso
description: Usar o telecine inverso
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows SDK de Formato de Mídia, telegráfica inversa
- Windows SDK de Formato de Mídia, tele meio
- ASF (Advanced Systems Format), inverse telejor
- ASF (Formato de Sistemas Avançados), telegráfica inversa
- ASF (Advanced Systems Format), tele artificial
- ASF (Formato de Sistemas Avançados), tele artificial
- teletração inversa
- Telecine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7885caffea83460d73b1eca26dbfd94eb50d99ac4aa8589113875ffc4358c029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585316"
---
# <a name="to-use-inverse-telecine"></a>Usar o telecine inverso

Teleia é o processo de conversão de filme, que tem 24 quadros por segundo, em vídeo, que tem 60 campos (metade quadros) por segundo. Esse processo coloca imagens de cada quadro de filme em vários campos de vídeo.

Quando você codifica digitalmente um vídeo que foi criado a partir de um filme usando tele circular, o processo de compactação pode causar artefatos de movimento e outras degradaçãos na qualidade. Para evitar afetar a qualidade da saída digital, o codec Windows Media Video 9 dá suporte à telegráfica inversa. Ao usar a telegráfica inversa, o codec reconstrói os 24 quadros de filme originais por segundo do vídeo de entrada antes de codificar o conteúdo.

Para usar a telegráfica inversa, você deve:

-   Use um perfil com um fluxo de vídeo definido como 24 quadros por segundo.
-   Conheça a configuração de campo do vídeo de entrada.

Para usar a telegráfica inversa para uma entrada para o autor, execute as etapas a seguir.

1.  Configurar o autor como de costume. Para obter mais informações, consulte [Escrevendo arquivos ASF](writing-asf-files.md).
2.  Antes de começar a escrever exemplos, obtenha um ponteiro para a interface [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) chamando **IWMWriter::QueryInterface**.
3.  Identifique o fluxo a ser reconstruído chamando [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para o número de entrada desejado. Passe g \_ wszDeintermode como a configuração e WM \_ DM \_ DEINTERMOD \_ INVERSETELE TOTAL como o valor.
4.  Chame **SetInputSetting** novamente para definir g \_ wszInitialPatternForInverseTelelore.
5.  Escreva o arquivo como de costume.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> <dt>

[**IWMWriter Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**IWMWriterAdvanced2 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




