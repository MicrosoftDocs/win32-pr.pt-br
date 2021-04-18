---
description: O exemplo de código a seguir demonstra como criar um objeto de chamada, descobrir os fluxos associados à chamada, selecionar e criar terminais apropriados, selecionar os terminais nos fluxos e concluir a conexão.
ms.assetid: 49815b18-a8ea-46e0-b2a4-3d7a82e727b0
title: Fazer uma chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc22ebde34e65c9acc8e6c7dd81944b06804935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759962"
---
# <a name="make-a-call"></a><span data-ttu-id="07954-103">Fazer uma chamada</span><span class="sxs-lookup"><span data-stu-id="07954-103">Make a Call</span></span>

<span data-ttu-id="07954-104">O exemplo de código a seguir demonstra como criar um objeto de chamada, descobrir os fluxos associados à chamada, selecionar e criar terminais apropriados, selecionar os terminais nos fluxos e concluir a conexão.</span><span class="sxs-lookup"><span data-stu-id="07954-104">The following code example demonstrates how to create a call object, discover the streams associated with the call, select and create appropriate terminals, select the terminals onto the streams, and complete the connection.</span></span>

<span data-ttu-id="07954-105">Antes de usar este exemplo de código, você deve executar as operações em [inicializar TAPI](initialize-tapi.md) e [selecionar um endereço](select-an-address.md).</span><span class="sxs-lookup"><span data-stu-id="07954-105">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md) and [Select an Address](select-an-address.md).</span></span>

<span data-ttu-id="07954-106">Além disso, você deve executar as operações ilustradas em [selecionar um terminal](select-a-terminal.md) seguindo a chamada para [**ITAddress:: createcall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall).</span><span class="sxs-lookup"><span data-stu-id="07954-106">Also, you must perform the operations illustrated in [Select a Terminal](select-a-terminal.md) following the call to [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall).</span></span>

> [!Note]  
> <span data-ttu-id="07954-107">Este exemplo não tem a verificação de erros e as versões apropriadas para o código de produção.</span><span class="sxs-lookup"><span data-stu-id="07954-107">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// Specify the destination address.
//
// szAddressToCall and 
// dwAddressType have been
// retrieved from a user interface.
ITBasicCallControl * pBasicCall
bstrAddressToCall = SysAllocString( szAddressToCall );
// If ( bstrAddressToCall == NULL ) process the error here. 

HRESULT hr = pAddress->CreateCall(
    bstrAddressToCall,
    dwAddressType,
    &pBasicCall
 );
// If ( hr != S_OK ) process the error here. 

SysFreeString(bstrAddressToCall);

// Create the required terminals for this call.
{
    // See the Select a Terminal code example.
}

// Make the connection.
pBasicCall->Connect( TRUE );
```

## <a name="related-topics"></a><span data-ttu-id="07954-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="07954-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07954-109">**ITAddress:: createchama**</span><span class="sxs-lookup"><span data-stu-id="07954-109">**ITAddress::CreateCall**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)
</dt> <dt>

[<span data-ttu-id="07954-110">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="07954-110">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="07954-111">**ITBasicCallControl:: conectar**</span><span class="sxs-lookup"><span data-stu-id="07954-111">**ITBasicCallControl::Connect**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)
</dt> </dl>

 

 



