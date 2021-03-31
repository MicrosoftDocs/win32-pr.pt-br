---
title: Usando os métodos de retorno de chamada
description: Usando os métodos de retorno de chamada
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- SDK do Windows Media Format, métodos de retorno de chamada
- Windows Media Format SDK, métodos chamados de forma assíncrona
- métodos de retorno de chamada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640125"
---
# <a name="using-the-callback-methods"></a>Usando os métodos de retorno de chamada

Várias interfaces no SDK do Windows Media Format contêm métodos que são chamados de forma assíncrona. A maioria desses métodos usa funções de retorno de chamada para passar informações para o aplicativo de controle.

As seções a seguir descrevem alguns dos problemas gerais relacionados ao uso de métodos de retorno de chamada com o SDK do Windows Media Format.



| Seção                                                                          | Descrição                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Usando o retorno de chamada OnStatus](using-the-onstatus-callback.md)                   | Descreve como implementar o método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , que é usado por vários objetos para aconselhar aplicativos de andamento da operação do SDK. |
| [Usando eventos com chamadas assíncronas](using-events-with-asynchronous-calls.md) | Descreve uma técnica comum para lidar com chamadas de método assíncrono em um aplicativo.                                                                                                                  |
| [Usando o parâmetro context](using-the-context-parameter.md)                   | Apresenta o parâmetro *pvContext* , compartilhado por vários retornos de chamada e seus métodos de chamada, e explica como usá-lo.                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 




