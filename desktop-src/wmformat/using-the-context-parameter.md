---
title: Usando o parâmetro context
description: Usando o parâmetro context
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- SDK do Windows Media Format, parâmetro de contexto
- SDK do Windows Media Format, parâmetro pvContext
- parâmetro pvContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084344"
---
# <a name="using-the-context-parameter"></a>Usando o parâmetro context

Alguns dos retornos de chamada usados pelo Windows Media Format SDK usam um parâmetro chamado *pvContext*. Os objetos de chamada passam pelo valor especificado no método que iniciou a ação assíncrona. Por exemplo, ao chamar [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), você pode passar um valor para *pvContext*. Quando o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) é chamado pelo objeto Reader para notificar seu aplicativo de que o arquivo foi aberto, ele passará qualquer valor usado em sua chamada para **Open** como o parâmetro *pvContext* de **OnStatus**. Esse parâmetro de contexto é fornecido para seu uso e você pode usá-lo da maneira que desejar.

O parâmetro *pvContext* é usado com mais frequência quando vários objetos precisam compartilhar o mesmo retorno de chamada. Por exemplo, vários objetos usam o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Você pode usar *pvContext* para permitir que os diferentes objetos compartilhem uma implementação de **OnStatus** passando um valor diferente para *pvContext* em sua chamada original. Em sua implementação de **OnStatus**, você pode ramificar a lógica de manipulação de mensagens com base no valor de *pvContext*.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando os métodos de retorno de chamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




