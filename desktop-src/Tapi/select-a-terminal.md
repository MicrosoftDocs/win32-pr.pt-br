---
description: O exemplo de código a seguir demonstra como selecionar terminais em fluxos associados a uma chamada.
ms.assetid: ff43e81c-ff39-466d-870a-54b75c2938a4
title: Selecionar um terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3d195e021f5937c733f3d7a0efce0cfee5eba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766210"
---
# <a name="select-a-terminal"></a>Selecionar um terminal

O exemplo de código a seguir demonstra como selecionar terminais em fluxos associados a uma chamada.

Antes de usar este exemplo de código, você deve executar as operações em [inicializar TAPI](initialize-tapi.md) e [selecionar um endereço](select-an-address.md).

Além disso, este exemplo requer que o aplicativo já tenha um ponteiro para a interface [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) de uma chamada de entrada ou saída. Consulte [fazer uma chamada](make-a-call.md) ou [receber uma chamada](receive-a-call.md) para obter exemplos de código sobre como obter esse ponteiro.

> [!Note]  
> Este exemplo não tem a verificação de erros e as versões apropriadas para o código de produção.

 

``` syntax
// pAddress is an ITAddress interface pointer.
// pBasicCall is an ITBasicCallControl interface pointer.

// Get the ITStreamControl interface.
ITStreamControl * pStreamControl;
HRESULT hr = pBasicCall->QueryInterface(
        IID_ITStreamControl,
        (void **) &pStreamControl
        );
// If ( hr != S_OK ) process the error here. 

// Enumerate the streams and select 
// terminals onto them.
IEnumStream * pEnumStreams;
ITStream    * pStream;
hr = pStreamControl->EnumerateStreams(&pEnumStreams);
// If ( hr != S_OK ) process the error here. 

while ( S_OK == pEnumStreams->Next(1, &pStream, NULL) )
{
    // Get the media type and direction of this stream.
    long                lMediaType;
    TERMINAL_DIRECTION  dir;
    hr = pStream->get_MediaType( &lMediaType );
    // If ( hr != S_OK ) process the error here. 
    hr = pStream->get_Direction( &dir );
    // If ( hr != S_OK ) process the error here. 

    // Create the default terminal for this media type and direction.
    //   If lMediaType == TAPIMEDIATYPE_VIDEO and
    //   dir == TD_RENDER, a dynamic video render terminal
    //   is required. Please see Incoming.cpp in 
    //   the samples section of the SDK. 
    // For all other terminals, get the default static terminal.
    ITTerminal * pTerminal;
    ITTerminalSupport * pTerminalSupport;
    hr = pAddress->QueryInterface( 
            IID_ITTerminalSupport, 
            (void **)&pTerminalSupport
         );
    // If ( hr != S_OK ) process the error here. 
    hr = pTerminalSupport->GetDefaultStaticTerminal(
            lMediaType,
            dir,
            pTerminal
         );
    // If ( hr != S_OK ) process the error here. 
    // Select the terminal on the stream.
    hr = pStream->SelectTerminal(pTerminal);
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> <dt>

[**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
