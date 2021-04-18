---
title: Gravando amostras compactadas
description: Gravando amostras compactadas
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- ASF (Advanced Systems Format), gravando amostras compactadas
- ASF (formato de sistemas avançados), gravando amostras compactadas
- ASF (Advanced Systems Format), passando amostras compactadas
- ASF (formato de sistemas avançados), passando amostras compactadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104453848"
---
# <a name="writing-compressed-samples"></a>Gravando amostras compactadas

Para alguns fluxos de áudio ou vídeo, talvez você queira passar exemplos que já foram compactados em vez de passar dados brutos. Esse recurso é usado para copiar um fluxo existente ou para escrever amostras compactadas com um codec de terceiros. O processo de gravar um exemplo compactado é idêntico a escrever um exemplo descompactado, exceto pelo fato de que você usa [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) em vez de [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Para obter mais informações sobre como escrever amostras descompactadas, consulte [para escrever exemplos](to-write-samples.md).

Quando você escreve amostras compactadas, para perfis de CBR, o gravador descartará alguns exemplos, se necessário, para manter o conteúdo dentro dos valores de janela de buffer e taxa de bits especificados. Para a VBR, o gravador não descartará amostras, mas não há como garantir que os valores de taxa de bits e de janela de buffer estejam corretos.

Se você estiver copiando um fluxo de um arquivo para outro, sempre deverá copiar o objeto de configuração de fluxo do perfil do arquivo original para o perfil do novo arquivo. Isso garante que você tenha a taxa de bits e as informações de janela de buffer corretas. Se você copiar um fluxo compactado para um fluxo que tenha uma janela de buffer inferior definida, os exemplos serão removidos durante a gravação do arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




