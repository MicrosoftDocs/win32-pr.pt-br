---
title: Usando eventos com chamadas assíncronas
description: Usando eventos com chamadas assíncronas
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows SDK do formato de mídia, eventos com chamadas assíncronas
- Windows SDK do formato de mídia, eventos de chamada assíncrona
- eventos, chamadas assíncronas
- eventos de chamada assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd315b56570419afd81aa3300cfa3ee1dd907e22310aba79432e4533f99a82db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929126"
---
# <a name="using-events-with-asynchronous-calls"></a>Usando eventos com chamadas assíncronas

Frequentemente, ao usar métodos que são chamados de forma assíncrona, você desejará interromper o processamento adicional de seu aplicativo até que o método conclua o processamento. Você pode implementar qualquer técnica que desejar para lidar com essa situação. Esta seção descreve como usar um evento para aguardar chamadas assíncronas no thread de chamada. essa técnica é frequentemente usada com o SDK do formato de mídia Windows e é demonstrada em alguns dos aplicativos de exemplo.

A lista a seguir resume o uso de eventos para aguardar chamadas assíncronas.

1.  Crie um evento para usar com seu aplicativo chamando a função **CreateEvent** do SDK da plataforma.
2.  Ao implementar os retornos de chamada apropriados para seu aplicativo, intercepte as mensagens para as quais você precisa aguardar. Na lógica de tratamento de mensagens para as mensagens desejadas, sinalize o evento chamando a função **SetEvent** do SDK da plataforma.
3.  Depois que as chamadas para eventos assíncronos são feitas em seu aplicativo, aguarde o evento ser sinalizado chamando a função **WaitForSingleObject** do Platform SDK. se você estiver criando um aplicativo Windows, deverá criar um loop para verificar Windows mensagens e incluir uma chamada para **WaitForSingleObject** no loop com um tempo de espera curto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando os métodos de retorno de chamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




