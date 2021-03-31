---
title: Gravando fluxos de imagem
description: Gravando fluxos de imagem
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- ASF (Advanced Systems Format), gravando fluxos de imagem
- ASF (formato de sistemas avançados), gravando fluxos de imagem
- ASF (Advanced Systems Format), fluxos de imagem
- ASF (formato de sistemas avançados), fluxos de imagem
- fluxos de imagem, gravando
- fluxos, gravando fluxos de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916994"
---
# <a name="writing-image-streams"></a>Gravando fluxos de imagem

As entradas para um fluxo de imagem devem ser imagens de bitmap formatadas em RGB. O gravador coordena a compactação de exemplos de imagem de entrada usando o formato JPEG. Antes de começar a gravar um arquivo que contém um fluxo de imagem, você deve definir uma qualidade de imagem para a entrada, usando a \_ configuração g wszJPEGCompressionQuality. Use [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para definir a qualidade para um valor **DWORD** que varia de 1 a 100. Valores baixos representam uma alta taxa de compactação às custas da qualidade, enquanto valores altos produzem imagens de alta qualidade que exigem mais espaço.

Os fluxos de imagem geralmente exigem janelas de buffer maiores do que fluxos de vídeo comuns. O tamanho exato necessário depende do tipo de imagem e da qualidade da imagem, entre outros fatores. Use a avaliação e o erro para determinar o tamanho apropriado para as imagens que você pretende processar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Fluxos de imagem**](image-streams.md)
</dt> <dt>

[**Para definir as configurações de entrada**](to-set-input-settings.md)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




