---
description: Configurando o log de erros
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: Configurando o log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac96fb90570408ca41be06656f7cf1704e9f48dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754209"
---
# <a name="setting-the-error-log"></a>Configurando o log de erros

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Depois de implementar a classe de log de erros, crie uma nova instância da classe. Em seguida, dê aos [serviços de edição do DirectShow](directshow-editing-services.md) um ponteiro para ele chamando o método [**IAMSetErrorLog::p UT log de \_ erros**](iamseterrorlog-put-errorlog.md) na linha do tempo. Consulte a linha do tempo para a interface **IAMSetErrorLog** . Para garantir que todos os erros sejam registrados, você deve chamar esse método antes de carregar, salvar ou renderizar a linha do tempo.


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



O log de erros não tem nenhum efeito sobre os valores de retorno que você recebe ao chamar métodos em seu aplicativo. O log de erros complementa, mas não substitui as técnicas de tratamento de erros usuais. Para criar um aplicativo robusto, sempre verifique os valores HRESULT.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erros de log](logging-errors.md)
</dt> </dl>

 

 



