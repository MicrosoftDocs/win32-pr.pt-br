---
title: Usando eventos com chamadas assíncronas
description: Usando eventos com chamadas assíncronas
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- SDK do Windows Media Format, eventos com chamadas assíncronas
- SDK do Windows Media Format, eventos de chamada assíncrona
- eventos, chamadas assíncronas
- eventos de chamada assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364326"
---
# <a name="using-events-with-asynchronous-calls"></a>Usando eventos com chamadas assíncronas

Frequentemente, ao usar métodos que são chamados de forma assíncrona, você desejará interromper o processamento adicional de seu aplicativo até que o método conclua o processamento. Você pode implementar qualquer técnica que desejar para lidar com essa situação. Esta seção descreve como usar um evento para aguardar chamadas assíncronas no thread de chamada. Essa técnica é frequentemente usada com o Windows Media Format SDK e é demonstrada em alguns dos aplicativos de exemplo.

A lista a seguir resume o uso de eventos para aguardar chamadas assíncronas.

1.  Crie um evento para usar com seu aplicativo chamando a função **CreateEvent** do SDK da plataforma.
2.  Ao implementar os retornos de chamada apropriados para seu aplicativo, intercepte as mensagens para as quais você precisa aguardar. Na lógica de tratamento de mensagens para as mensagens desejadas, sinalize o evento chamando a função **SetEvent** do SDK da plataforma.
3.  Depois que as chamadas para eventos assíncronos são feitas em seu aplicativo, aguarde o evento ser sinalizado chamando a função **WaitForSingleObject** do Platform SDK. Se você estiver criando um aplicativo do Windows, deverá criar um loop para verificar se há mensagens do Windows e incluir uma chamada para **WaitForSingleObject** no loop com um tempo de espera curto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando os métodos de retorno de chamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




