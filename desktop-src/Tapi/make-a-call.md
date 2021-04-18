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
# <a name="make-a-call"></a>Fazer uma chamada

O exemplo de código a seguir demonstra como criar um objeto de chamada, descobrir os fluxos associados à chamada, selecionar e criar terminais apropriados, selecionar os terminais nos fluxos e concluir a conexão.

Antes de usar este exemplo de código, você deve executar as operações em [inicializar TAPI](initialize-tapi.md) e [selecionar um endereço](select-an-address.md).

Além disso, você deve executar as operações ilustradas em [selecionar um terminal](select-a-terminal.md) seguindo a chamada para [**ITAddress:: createcall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall).

> [!Note]  
> Este exemplo não tem a verificação de erros e as versões apropriadas para o código de produção.

 

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

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ITAddress:: createchama**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITBasicCallControl:: conectar**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)
</dt> </dl>

 

 



