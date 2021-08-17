---
title: Suporte a DRM no DirectShow
description: Suporte a DRM no DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows SDK de Formato de Mídia, suporte a DRM em DirectShow
- Windows SDK de formato de mídia, DirectShow
- Windows SDK de Formato de Mídia, DRM (gerenciamento de direitos digitais)
- AsF (Advanced Systems Format), suporte a DRM em DirectShow
- ASF (Formato de Sistemas Avançados), suporte a DRM no DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), DRM (gerenciamento de direitos digitais)
- ASF (Formato de Sistemas Avançados), DRM (gerenciamento de direitos digitais)
- DirectShow, suporte a DRM
- DRM (gerenciamento de direitos digitais), DirectShow
- DRM (gerenciamento de direitos digitais), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b3de3ca80d1b3b2fe27c9af590fe0cba0202b1fdd9b6fc322d8ed1c1871536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930876"
---
# <a name="drm-support-in-directshow"></a>Suporte a DRM no DirectShow

Ler e escrever arquivos protegidos por DRM no DirectShow é feito basicamente da mesma maneira que quando você usa o SDK Windows Formato de Mídia diretamente. Para começar, você precisa da biblioteca estática wmstubdrm, que é obtida separadamente da Microsoft. Além disso, você deve implementar a interface **IKeyProvider** para permitir que seu aplicativo acesse os objetos de tempo de execução do SDK de Formato de Mídia Windows quando o DRM estiver habilitado.

Ao aplicar a proteção DRM versão 1, use a interface [**IWMHeaderInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) que é obtida conforme descrito em Lendo arquivos [ASF no DirectShow](reading-asf-files-in-directshow.md). Ao aplicar a proteção DRM versão 7, obtenha a interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) chamando **QueryService** no filtro [Wm ASF Writer,](wm-asf-writer-filter.md) conforme mostrado no snippet de código mais adiante neste tópico.

Todas as outras configurações específicas do DRM são exatamente as mesmas descritas em [Habilitando o suporte a DRM.](enabling-drm-support.md) Use **QueryService** para obter a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) do filtro [Leitor do WM ASF.](wm-asf-reader-filter.md)

O DirectX 9.0 contém um exemplo, PlayWndASF, um aplicativo de player de DirectShow habilitado para DRM que demonstra a aquisição de licença do DRM versão 1 e versão 7. Este exemplo também inclui uma implementação da **classe CKeyProvider,** que dá suporte à interface **IKeyProvider.**

 

 




