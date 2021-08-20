---
title: Plug-ins de origem
description: Plug-ins de origem
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Windows SDK do formato de mídia, plug-ins de origem
- ASF (Advanced Systems Format), plug-ins de origem
- ASF (formato de sistemas avançados), plug-ins de origem
- plug-ins de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f16d0edc82423a43e50591fa07e14623adc23b94234a28985afca8a496822a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845800"
---
# <a name="source-plug-ins"></a>Plug-ins de origem

um plug-in de origem é uma opção disponível para os desenvolvedores que desejam implementar seu próprio sistema de armazenamento para arquivos de Windows de mídia®. Um plug-in de origem permite isso por meio da implementação de uma interface COM chamada **IStream**, que é uma interface padrão para fornecer dados.

O plug-in de origem deve ser gravado como uma dll e sua presença é conhecida pelo SDK por meio de uma entrada de registro. Pode haver qualquer número de plug-ins de origem implementados dessa maneira. O plug-in de origem deve exportar a função [**WMCreateStreamForURL**](wmcreatestreamforurl.md) .

Para registrar um plug-in de origem, a seguinte entrada de registro deve ser adicionada:

HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows Media \\ WMSDK \\ sources

Name = "qualquer nome exclusivo"

Valor = nome do caminho da DLL de plug-in de origem

Depois que a DLL tiver sido registrada, o aplicativo poderá usar o método **IWMReader:: Open** (com a URL apropriada como um parâmetro) para acessar dados de fluxo, que podem ser armazenados em arquivos ou contêineres de dados definidos pelo usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMReader:: abrir**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> <dt>

[**WMCreateStreamForURL**](wmcreatestreamforurl.md)
</dt> </dl>

 

 




