---
description: Os monitores de rede chamam a função RecognizeFrame de um analisador para determinar se o analisador reconhece os dados não reivindicados de um quadro.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implementando RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970eee80a04168b3fa06b117c2c219c506da7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297438"
---
# <a name="implementing-recognizeframe"></a>Implementando RecognizeFrame

Os monitores de rede chamam a função [**RecognizeFrame**](recognizeframe.md) de um analisador para determinar se o analisador reconhece os dados não reivindicados de um quadro. Os dados não reivindicados podem estar no início de um quadro, mas normalmente os dados não reivindicados estão localizados no meio de um quadro. A ilustração a seguir mostra os dados não reivindicados localizados no meio de um quadro.

![dados não reivindicados localizados no meio de um quadro](images/recognizeframe1.png)

Monitor de Rede fornece as seguintes informações ao chamar a função [**RecognizeFrame**](recognizeframe.md) :

-   Um identificador para o quadro.
-   Um ponteiro para o início do quadro.
-   Um ponteiro para o início dos dados não reivindicados.
-   O valor MAC do primeiro protocolo no quadro.
-   O número de bytes nos dados não reivindicados; ou seja, os bytes restantes no quadro.
-   Um identificador para o protocolo anterior.
-   O deslocamento do protocolo anterior.

Quando a DLL do analisador determina que os dados não reivindicados começam com o protocolo do analisador, a DLL do analisador determina o local em que o próximo protocolo começa e o seguinte protocolo. A DLL do analisador funciona nas seguintes maneiras condicionais:

-   Se a DLL do analisador reconhecer dados não reivindicados, a DLL do analisador definirá o parâmetro *pProtocolStatus* e retornará um ponteiro para o próximo protocolo no quadro, ou **NULL**. **NULL** será retornado se o protocolo atual for o último protocolo no quadro.
-   Se a DLL do analisador reconhecer dados não reivindicados e identificar o protocolo a seguir (das informações fornecidas no protocolo), a DLL do analisador retornará um ponteiro para o identificador do próximo protocolo no parâmetro *phNextProtocol* da função.
-   Se a DLL do analisador não reconhecer dados não reivindicados, a DLL do analisador retornará o ponteiro para o início de dados não reivindicados e Monitor de Rede continuará tentando analisar os dados não reivindicados.

**Para implementar o RecognizeFrame**

1.  Teste para determinar se você reconhece o protocolo.
2.  Se você reconhece dados não reivindicados e sabe qual protocolo segue, defina *pProtocolStatus* como protocolo do \_ próximo protocolo do status \_ \_ , defina *phNextProtocol* como um ponteiro que aponte para o identificador do próximo protocolo e, em seguida, retorne um ponteiro para o próximo protocolo.

    –ou–

    Se você reconhece dados não reivindicados e não sabe qual protocolo segue, defina *pProtocolStatus* para status de protocolo \_ \_ reconhecido e, em seguida, retorne um ponteiro para o próximo protocolo.

    –ou–

    Se você reconhece dados não reivindicados e seu protocolo é o último protocolo em um quadro, defina *pProtocolStatus* para status de protocolo \_ \_ declarado e, em seguida, retorne **nulo**.

    –ou–

    Se você não reconhecer dados não reivindicados, defina *pProtocolStatus* como status de \_ protocolo \_ não \_ reconhecido e, em seguida, retorne o ponteiro que é passado para você em *pProtocol*.

Veja a seguir uma implementação básica do [**RecognizeFrame**](recognizeframe.md).

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

 

 



