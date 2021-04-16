---
title: Plug-ins de origem
description: Plug-ins de origem
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- SDK do Windows Media Format, plug-ins de origem
- ASF (Advanced Systems Format), plug-ins de origem
- ASF (formato de sistemas avançados), plug-ins de origem
- plug-ins de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4822b9110def4e1b758be40310f503fd56a251fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105772670"
---
# <a name="source-plug-ins"></a>Plug-ins de origem

Um plug-in de origem é uma opção disponível para os desenvolvedores que desejam implementar seu próprio sistema de armazenamento para arquivos do Windows Media®. Um plug-in de origem permite isso por meio da implementação de uma interface COM chamada **IStream**, que é uma interface padrão para fornecer dados.

O plug-in de origem deve ser gravado como uma dll e sua presença é conhecida pelo SDK por meio de uma entrada de registro. Pode haver qualquer número de plug-ins de origem implementados dessa maneira. O plug-in de origem deve exportar a função [**WMCreateStreamForURL**](wmcreatestreamforurl.md) .

Para registrar um plug-in de origem, a seguinte entrada de registro deve ser adicionada:

HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Media \\ WMSDK \\ sources

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

 

 




