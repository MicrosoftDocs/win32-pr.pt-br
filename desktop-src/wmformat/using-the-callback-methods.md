---
title: Usando os métodos de retorno de chamada
description: Usando os métodos de retorno de chamada
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows SDK do formato de mídia, métodos de retorno de chamada
- Windows SDK do formato de mídia, métodos chamados de forma assíncrona
- métodos de retorno de chamada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ee2bcf6587e2e9e75e18404a60c3b85fb4bac5e9f14fd0164304bcc3f3338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110056"
---
# <a name="using-the-callback-methods"></a>Usando os métodos de retorno de chamada

várias interfaces no SDK do formato de mídia Windows contêm métodos que são chamados de forma assíncrona. A maioria desses métodos usa funções de retorno de chamada para passar informações para o aplicativo de controle.

as seções a seguir descrevem alguns dos problemas gerais relacionados ao uso de métodos de retorno de chamada com o SDK do formato de mídia Windows.



| Seção                                                                          | Descrição                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Usando o retorno de chamada OnStatus](using-the-onstatus-callback.md)                   | Descreve como implementar o método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , que é usado por vários objetos para aconselhar aplicativos de andamento da operação do SDK. |
| [Usando eventos com chamadas assíncronas](using-events-with-asynchronous-calls.md) | Descreve uma técnica comum para lidar com chamadas de método assíncrono em um aplicativo.                                                                                                                  |
| [Usando o parâmetro context](using-the-context-parameter.md)                   | Apresenta o parâmetro *pvContext* , compartilhado por vários retornos de chamada e seus métodos de chamada, e explica como usá-lo.                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 




