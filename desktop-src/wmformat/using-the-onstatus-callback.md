---
title: Usando o retorno de chamada OnStatus
description: Usando o retorno de chamada OnStatus
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- SDK do Windows Media Format, método de retorno de chamada OnStatus
- SDK do Windows Media Format, interface IWMStatusCallback
- Método de retorno de chamada OnStatus, sobre
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916970"
---
# <a name="using-the-onstatus-callback"></a>Usando o retorno de chamada OnStatus

O método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) é chamado por vários objetos no SDK do Windows Media Format. **OnStatus** recebe mensagens que representam as alterações no status das operações do SDK.

Para usar o método de retorno de chamada **OnStatus** , você deve implementar uma classe em seu aplicativo que herde da interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) . Inclua o código para sua versão do **OnStatus** na classe. Vários exemplos de implementações de **OnStatus** podem ser encontrados nos exemplos incluídos neste SDK. Para obter mais informações sobre os exemplos, consulte [aplicativos de exemplo](sample-applications.md).

Você deve associar sua implementação do retorno de chamada de status com vários objetos do Windows Media Format SDK. Cada objeto tem uma maneira diferente de fazer essa associação. Para obter uma lista dos métodos que associam objetos específicos, consulte a página de referência do **IWMStatusCallback** .

As mensagens de status que podem ser recebidas por **OnStatus** são definidas no tipo de enumeração [**\_ status WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .

Você pode escolher quais mensagens interceptar e quais ignorar. No entanto, responder a algumas mensagens de status é necessário para determinados recursos. Por exemplo, ao usar o leitor assíncrono, o método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) abre um arquivo de forma assíncrona. A única maneira de saber quando o arquivo foi aberto é interceptar a \_ mensagem aberta MWT. Normalmente, as mensagens às quais você responde são notificações sobre a conclusão de tarefas assíncronas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando os métodos de retorno de chamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




