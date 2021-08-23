---
title: Usando o parâmetro context
description: Usando o parâmetro context
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows SDK de Formato de Mídia, parâmetro de contexto
- Windows SDK de Formato de Mídia, parâmetro pvContext
- Parâmetro pvContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102315470243910158fd3bf474a209fa1e0888536671e3ede3764be519c672f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585196"
---
# <a name="using-the-context-parameter"></a>Usando o parâmetro context

Alguns dos retornos de chamada usados pelo SDK Windows Formato de Mídia do Windows um parâmetro chamado *pvContext*. Os objetos de chamada passam o valor especificado no método que iniciou a ação assíncrona. Por exemplo, ao chamar [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), você pode passar um valor para *pvContext.* Quando o método [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) for chamado pelo objeto de leitor para notificar seu aplicativo de que o arquivo foi aberto, ele passará qualquer valor usado na chamada para **Abrir** como o parâmetro *pvContext* **de OnStatus**. Esse parâmetro de contexto é fornecido para seu uso e você pode usá-lo da maneira que quiser.

O *parâmetro pvContext* é usado com mais frequência quando vários objetos precisam compartilhar o mesmo retorno de chamada. Por exemplo, vários objetos usam o [**método IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Você pode usar *pvContext* para permitir que os diferentes objetos compartilhem uma implementação de **OnStatus** passando um valor diferente para *pvContext* em sua chamada original. Em sua implementação de **OnStatus**, você pode ramificar a lógica de tratamento de mensagem com base no valor *de pvContext*.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando os métodos de retorno de chamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




