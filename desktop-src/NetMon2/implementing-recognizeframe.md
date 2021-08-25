---
description: Monitores de Rede chama a função RecognizeFrame de um analisador para determinar que o analisador reconhece os dados não confirmados de um quadro.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implementando RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d3f9a79325c0c75a7a83cfb99a34ff3de1f073573dee13d39a846b575f6285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890487"
---
# <a name="implementing-recognizeframe"></a>Implementando RecognizeFrame

Monitores de Rede chama a [**função RecognizeFrame**](recognizeframe.md) de um analisador para determinar que o analisador reconhece os dados não confirmados de um quadro. Os dados não confirmados podem estar no início de um quadro, mas normalmente, os dados não confirmados estão localizados no meio de um quadro. A ilustração a seguir mostra dados não confirmados localizados no meio de um quadro.

![dados não confirmados localizados no meio de um quadro](images/recognizeframe1.png)

Monitor de Rede fornece as seguintes informações quando chama a [**função RecognizeFrame:**](recognizeframe.md)

-   Um alça para o quadro.
-   Um ponteiro para o início do quadro.
-   Um ponteiro para o início dos dados não confirmados.
-   O valor MAC do primeiro protocolo no quadro.
-   O número de bytes nos dados não confirmados; ou seja, os bytes restantes no quadro.
-   Um alça para o protocolo anterior.
-   O deslocamento do protocolo anterior.

Quando a DLL do analisador determina que os dados não confirmados começam com o protocolo do analisador, a DLL do analisador determina onde o próximo protocolo é iniciado e qual protocolo segue. A DLL do analisador funciona das seguintes maneiras condicionais:

-   Se a DLL do analisador reconhecer dados não confirmados, a DLL do analisador define o parâmetro *pProtocolStatus* e retorna um ponteiro para o próximo protocolo no quadro ou **NULL.** **NULL** será retornado se o protocolo atual for o último protocolo no quadro.
-   Se a DLL do analisador reconhecer dados não confirmados e identificar o protocolo a seguir (das informações fornecidas no protocolo), a DLL do analisador retornará um ponteiro para o identificador do próximo protocolo no parâmetro *phNextProtocol* da função.
-   Se a DLL do analisador não reconhecer dados não confirmados, a DLL do analisador retornará o ponteiro para o início dos dados não Monitor de Rede continuará tentando analisar os dados não confirmados.

**Para implementar o RecognizeFrame**

1.  Teste para determinar se você reconhece o protocolo.
2.  Se você reconhecer dados não confirmados e sabe qual protocolo segue, desmarque *pProtocolStatus* como PROTOCOLO STATUS NEXT PROTOCOL, desmarque \_ \_ \_ *phNextProtocol* como um ponteiro que aponta para o ponteiro para o próximo protocolo e, em seguida, retorne um ponteiro para o próximo protocolo.

    –ou–

    Se você reconhecer dados não confirmados e não sabe qual protocolo segue, desmarque *pProtocolStatus* como STATUS DE PROTOCOLO RECONHECIDO e, em seguida, retorne um ponteiro para o \_ \_ próximo protocolo.

    –ou–

    Se você reconhecer dados não reivindicados e seu protocolo for o último protocolo em um quadro, demarque *pProtocolStatus* como STATUS DO PROTOCOLO \_ REIVINDICADO e, em seguida, retorne \_ **NULL**.

    –ou–

    Se você não reconhecer dados não confirmados, demarque *pProtocolStatus* como STATUS DE PROTOCOLO NÃO RECONHECIDO e, em seguida, retorne o ponteiro que é passado para você \_ \_ em \_ *pProtocol*.

A seguir está uma implementação básica do [**RecognizeFrame.**](recognizeframe.md)

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



