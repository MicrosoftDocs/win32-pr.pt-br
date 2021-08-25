---
title: Escrevendo imagens Fluxos
description: Escrevendo imagens Fluxos
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- ASF (Advanced Systems Format), escrevendo fluxos de imagem
- ASF (Formato de Sistemas Avançados), escrevendo fluxos de imagem
- ASF (Advanced Systems Format), fluxos de imagem
- ASF (Formato de Sistemas Avançados), fluxos de imagem
- fluxos de imagem, escrevendo
- fluxos, escrevendo fluxos de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6061af2ff43cbeb3fe688b6533eee044036df029bdb7f7305af305c8d45084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006296"
---
# <a name="writing-image-streams"></a>Escrevendo imagens Fluxos

As entradas para um fluxo de imagem devem ser imagens de bitmap formatadas em RGB. O autor coordena a compactação de exemplos de imagem de entrada usando o formato JPEG. Antes de começar a escrever um arquivo que contém um fluxo de imagem, você deve definir uma qualidade de imagem para a entrada, usando a configuração \_ g wszJPEGCompressionQuality. Use [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para definir a qualidade como um **valor DWORD** que varia de 1 a 100. Valores baixos representam uma alta taxa de compactação às custas da qualidade, enquanto valores altos produzem imagens de alta qualidade que exigem mais espaço.

Os fluxos de imagem geralmente exigem janelas de buffer maiores do que fluxos de vídeo comuns. O tamanho exato necessário depende do tipo de imagem e da qualidade da imagem, entre outros fatores. Use a avaliação e o erro para determinar o tamanho apropriado para as imagens que você pretende processar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Imagem Fluxos**](image-streams.md)
</dt> <dt>

[**Para definir a entrada Configurações**](to-set-input-settings.md)
</dt> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




