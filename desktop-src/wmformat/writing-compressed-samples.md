---
title: Escrevendo exemplos compactados
description: Escrevendo exemplos compactados
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- ASF (Advanced Systems Format), escrevendo exemplos compactados
- ASF (Formato de Sistemas Avançados), escrevendo exemplos compactados
- ASF (Advanced Systems Format), passando amostras compactadas
- ASF (Formato de Sistemas Avançados), passando amostras compactadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaa6bf5298e465716fe7a60eb5de2459f09be405611ac7322b534804bbbc997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843650"
---
# <a name="writing-compressed-samples"></a>Escrevendo exemplos compactados

Para alguns fluxos de áudio ou vídeo, talvez você queira passar exemplos que já estão compactados em vez de passar dados brutos. Esse recurso é usado para copiar um fluxo existente ou para gravar exemplos compactados com um codec de terceiros. O processo de gravação de uma amostra compactada é idêntico à gravação de um exemplo descompactado, exceto pelo fato de que você usa [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) em vez [**de IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Para obter mais informações sobre como escrever exemplos descompactados, consulte [To Write Samples](to-write-samples.md).

Quando você escreve exemplos compactados, para perfis CBR, o autor soltará alguns exemplos, se necessário, para manter o conteúdo dentro da taxa de bits e dos valores de janela de buffer especificados. Para a VBR, o autor não soltará amostras, mas não é possível ter certeza de que os valores de taxa de bits e janela de buffer estarão corretos.

Se você estiver copiando um fluxo de um arquivo para outro, sempre deverá copiar o objeto de configuração de fluxo do perfil do arquivo original para o perfil do novo arquivo. Isso garante que você tenha as informações corretas da taxa de bits e da janela do buffer. Se você copiar um fluxo compactado para um fluxo que tem um conjunto de janelas de buffer inferior, os exemplos serão descartados durante a escrita do arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




