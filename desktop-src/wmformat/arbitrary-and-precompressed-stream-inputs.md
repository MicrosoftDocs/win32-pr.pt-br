---
title: Entradas de fluxo arbitrárias e precompactadas
description: Entradas de fluxo arbitrárias e precompactadas
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- ASF (Advanced Systems Format), entradas de fluxo arbitrárias
- ASF (formato de sistemas avançados), entradas de fluxo arbitrárias
- perfis, entradas de fluxo arbitrários
- codecs, entradas de fluxo arbitrários
- Formato de sistema avançado (ASF), entradas de fluxo precompactados
- ASF (formato de sistemas avançados), entradas de fluxo precompactados
- perfis, entradas de fluxo precompactados
- codecs, entradas de fluxo compactados
- entradas de fluxo precompactadas
- entradas de fluxo arbitrários
- fluxos, entradas de fluxo arbitrários
- fluxos, entradas de fluxo compactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "105807319"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a>Entradas de fluxo arbitrárias e precompactadas

Somente as entradas que devem ser compactadas por um dos codecs de mídia do Windows têm várias entradas possíveis. Os outros tipos de entradas possíveis são entradas arbitrárias e entradas precompactadas. Os requisitos para formatos de entrada para esses tipos são descritos nesta seção.

## <a name="arbitrary-stream-inputs"></a>Entradas de fluxo arbitrários

As entradas para tipos de fluxo arbitrários são as mesmas que os formatos de fluxo descritos no perfil. Você não deve ter que definir formatos de entrada para esses tipos.

## <a name="precompressed-stream-inputs"></a>Entradas de fluxo precompactadas

Ao copiar um fluxo de um arquivo para outro, você passa por exemplos que já foram compactados. Nesse caso, você deve definir o objeto de propriedades de entrada como **nulo** para informar ao gravador que ele não precisa validar os dados que você está passando. Para definir o formato de entrada como **NULL**, chame [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passe **NULL** como o segundo parâmetro. Ao chamar esse método com um parâmetro **nulo** , você deve fazer a chamada antes de chamar [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Ao usar fluxos compactados, você deve copiar manualmente as informações do codec para o cabeçalho do arquivo antes de gravar. Para obter as informações do codec, chame [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar os codecs associados ao arquivo no leitor. Selecione as informações de codec que correspondem à configuração de fluxo do fluxo precompactado. Em seguida, defina as informações do codec no gravador chamando [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando as informações obtidas do leitor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> </dl>

 

 




