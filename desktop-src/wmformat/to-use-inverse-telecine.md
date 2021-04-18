---
title: Usar o telecine inverso
description: Usar o telecine inverso
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- SDK do Windows Media Format, telecineon inverso
- SDK do Windows Media Format, telecineon
- Formato de sistema avançado (ASF), inverso
- ASF (formato de sistemas avançados), telecineon inverso
- Formato de sistema avançado (ASF), telecineon
- ASF (formato de sistemas avançados), telecineon
- inverso
- telecineon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4f4e3ae34c2a9efcaa4fe8e5ce7256474404
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105807249"
---
# <a name="to-use-inverse-telecine"></a>Usar o telecine inverso

Telecineon é o processo de conversão de filme, que tem 24 quadros por segundo, para vídeo, que tem 60 campos (metade de quadros) por segundo. Esse processo coloca imagens de cada quadro de filme em vários campos de vídeo.

Quando você codifica digitalmente um vídeo que foi criado do filme usando o telecineon, o processo de compactação pode causar artefatos de movimento e outras degradações na qualidade. Para evitar afetar a qualidade da saída digital, o codec do Windows Media Video 9 dá suporte ao telecineon inverso. Ao usar o telecineon inverso, o codec reconstrói os 24 quadros de filme originais por segundo do vídeo de entrada antes de codificar o conteúdo.

Para usar o telecineon inverso, você deve:

-   Use um perfil com um fluxo de vídeo definido como 24 quadros por segundo.
-   Conheça a configuração de campo do vídeo de entrada.

Para usar o telecineon inverso para uma entrada para o gravador, execute as etapas a seguir.

1.  Configure o gravador como de costume. Para obter mais informações, consulte [Writing ASF files](writing-asf-files.md).
2.  Antes de começar a escrever amostras, obtenha um ponteiro para a interface [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) chamando **IWMWriter:: QueryInterface**.
3.  Identifique o fluxo a ser reconstruído chamando [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para o número de entrada desejado. Passe g \_ wszDeinterlaceMode como a configuração e o WM \_ DM \_ desentrelaçando \_ INVERSETELECINE como o valor.
4.  Chame **SetInputSetting** novamente para definir g \_ wszInitialPatternForInverseTelecine.
5.  Grave o arquivo como de costume.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Interface IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




