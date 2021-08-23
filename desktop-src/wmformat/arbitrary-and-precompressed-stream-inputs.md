---
title: Entradas de fluxo arbitrárias e pré-compactadas
description: Entradas de fluxo arbitrárias e pré-compactadas
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- ASF (Advanced Systems Format), entradas de fluxo arbitrárias
- ASF (Formato de Sistemas Avançados), entradas de fluxo arbitrárias
- perfis, entradas de fluxo arbitrárias
- codecs, entradas de fluxo arbitrárias
- ASF (Advanced Systems Format), entradas de fluxo pré-compactadas
- ASF (Formato de Sistemas Avançados), entradas de fluxo pré-compactadas
- perfis, entradas de fluxo pré-compactadas
- codecs, entradas de fluxo pré-compactadas
- entradas de fluxo pré-compactadas
- entradas de fluxo arbitrárias
- fluxos, entradas de fluxo arbitrárias
- fluxos, entradas de fluxo pré-compactadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0129362e8dc01b7ccf3faabbf10e22ffd4eccc082782796059b3cf4578c33a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448266"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a>Entradas de fluxo arbitrárias e pré-compactadas

Somente as entradas que devem ser compactadas por um dos codecs Windows Media têm várias entradas possíveis. Os outros tipos de entradas possíveis são entradas arbitrárias e entradas pré-compactadas. Os requisitos para formatos de entrada para esses tipos são descritos nesta seção.

## <a name="arbitrary-stream-inputs"></a>Entradas de fluxo arbitrárias

As entradas para tipos de fluxo arbitrários são as mesmas que os formatos de fluxo descritos no perfil. Você não deve ter que definir formatos de entrada para esses tipos.

## <a name="precompressed-stream-inputs"></a>Entradas de fluxo pré-compactadas

Ao copiar um fluxo de um arquivo para outro, você passa exemplos que já estão compactados. Nesse caso, você deve definir o objeto de propriedades de entrada como **NULL** para informar ao autor que ele não precisa validar os dados que você está passando. Para definir o formato de entrada como **NULL,** chame [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passe **NULL** como o segundo parâmetro. Ao chamar esse método com um **parâmetro NULL,** você deve fazer a chamada antes de [**chamar BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Ao usar fluxos pré-compactados, você deve copiar manualmente as informações de codec para o header do arquivo antes de escrever. Para obter as informações de codec, chame [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar os codecs associados ao arquivo no leitor. Selecione as informações de codec que corresponde à configuração de fluxo do fluxo pré-compactado. Em seguida, de definir as informações de codec no autor chamando [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando as informações obtidas do leitor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> </dl>

 

 




