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
# <a name="select-a-terminal"></a><span data-ttu-id="06832-103">Selecionar um terminal</span><span class="sxs-lookup"><span data-stu-id="06832-103">Select a Terminal</span></span>

<span data-ttu-id="06832-104">O exemplo de código a seguir demonstra como selecionar terminais em fluxos associados a uma chamada.</span><span class="sxs-lookup"><span data-stu-id="06832-104">The following code example demonstrates how to select terminals onto streams associated with a call.</span></span>

<span data-ttu-id="06832-105">Antes de usar este exemplo de código, você deve executar as operações em [inicializar TAPI](initialize-tapi.md) e [selecionar um endereço](select-an-address.md).</span><span class="sxs-lookup"><span data-stu-id="06832-105">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md) and [Select an Address](select-an-address.md).</span></span>

<span data-ttu-id="06832-106">Além disso, este exemplo requer que o aplicativo já tenha um ponteiro para a interface [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) de uma chamada de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="06832-106">Also, this example requires that the application already have a pointer to the [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) interface of either an incoming or outgoing call.</span></span> <span data-ttu-id="06832-107">Consulte [fazer uma chamada](make-a-call.md) ou [receber uma chamada](receive-a-call.md) para obter exemplos de código sobre como obter esse ponteiro.</span><span class="sxs-lookup"><span data-stu-id="06832-107">See [Make a Call](make-a-call.md) or [Receive a Call](receive-a-call.md) for code examples on how to obtain this pointer.</span></span>

> [!Note]  
> <span data-ttu-id="06832-108">Este exemplo não tem a verificação de erros e as versões apropriadas para o código de produção.</span><span class="sxs-lookup"><span data-stu-id="06832-108">This example does not have the error checking and releases appropriate for production code.</span></span>

 

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

## <a name="related-topics"></a><span data-ttu-id="06832-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06832-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06832-110">**ITAddress**</span><span class="sxs-lookup"><span data-stu-id="06832-110">**ITAddress**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)
</dt> <dt>

[<span data-ttu-id="06832-111">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="06832-111">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="06832-112">**ITStreamControl**</span><span class="sxs-lookup"><span data-stu-id="06832-112">**ITStreamControl**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)
</dt> <dt>

[<span data-ttu-id="06832-113">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="06832-113">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="06832-114">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="06832-114">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[<span data-ttu-id="06832-115">**ITTerminal**</span><span class="sxs-lookup"><span data-stu-id="06832-115">**ITTerminal**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> <dt>

[<span data-ttu-id="06832-116">**ITTerminalSupport**</span><span class="sxs-lookup"><span data-stu-id="06832-116">**ITTerminalSupport**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
