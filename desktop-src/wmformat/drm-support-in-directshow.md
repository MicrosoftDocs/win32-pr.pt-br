---
title: Suporte a DRM no DirectShow
description: Suporte a DRM no DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- SDK do Windows Media Format, suporte a DRM no DirectShow
- SDK do Windows Media Format, DirectShow
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- ASF (Advanced Systems Format), suporte a DRM no DirectShow
- ASF (formato de sistemas avançados), suporte a DRM no DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), DRM (gerenciamento de direitos digitais)
- ASF (formato de sistemas avançados), DRM (gerenciamento de direitos digitais)
- DirectShow, suporte a DRM
- DRM (gerenciamento de direitos digitais), DirectShow
- DRM (gerenciamento de direitos digitais), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916979"
---
# <a name="drm-support-in-directshow"></a>Suporte a DRM no DirectShow

A leitura e a gravação de arquivos protegidos por DRM no DirectShow é feita basicamente da mesma maneira que quando você usa o SDK do Windows Media Format diretamente. Para começar, você precisa da biblioteca estática wmstubdrm, que é obtida separadamente da Microsoft. Além disso, você deve implementar a interface **IKeyProvider** para permitir que seu aplicativo acesse os objetos de tempo de execução do Windows Media Format SDK quando o DRM estiver habilitado.

Ao aplicar a proteção do DRM versão 1, use a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , que é obtida conforme descrito em [lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md). Ao aplicar a proteção do DRM versão 7, obtenha a interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) chamando **QueryService** no filtro de [gravador ASF do WM](wm-asf-writer-filter.md) , conforme mostrado no trecho de código mais adiante neste tópico.

Todas as outras configurações específicas de DRM são exatamente as mesmas, conforme descrito em [habilitando o suporte a DRM](enabling-drm-support.md). Use o **QueryService** para obter a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) do filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .

O DirectX 9,0 contém um exemplo de PlayWndASF, um aplicativo de Player DirectShow habilitado para DRM que demonstra a aquisição de licença do DRM versão 1 e versão 7. Este exemplo também inclui uma implementação da classe **CKeyProvider** , que dá suporte à interface **IKeyProvider** .

 

 




