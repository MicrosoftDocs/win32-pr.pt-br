---
title: Interpretando informações de associação
description: O Microsoft RPC permite que seus programas de cliente e servidor acessem e interpretam as informações em um identificador de ligação.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- Chamada de procedimento remoto RPC, tarefas, interpretando Associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453719"
---
# <a name="interpreting-binding-information"></a>Interpretando informações de associação

O Microsoft RPC permite que seus programas de cliente e servidor acessem e interpretam as informações em um identificador de ligação. Isso não significa que você pode ou deve tentar acessar o conteúdo de um identificador de associação diretamente. O Microsoft RPC fornece funções que definem e recuperam as informações em identificadores de associação.

Para obter as informações em um identificador de ligação, passe o identificador para [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Ele retorna as informações de associação como uma cadeia de caracteres. Para cada chamada para **RpcBindingToStringBinding**, você deve ter uma chamada correspondente para a função [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).

Você pode chamar a função [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) para analisar a cadeia de caracteres Obtida de [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Essa função aloca cadeias de caracteres para conter as informações analisadas. Se você não quiser que ele analise uma parte específica das informações de associação, passe um **NULL** como o valor desse parâmetro. Certifique-se de chamar [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para cada uma das cadeias de caracteres alocadas.

O fragmento de código a seguir ilustra como um aplicativo pode chamar essas funções.


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



O código de exemplo anterior chama as funções [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) e [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) para obter e analisar as informações em um identificador de associação válido. Observe que o valor **NULL** foi passado como o segundo parâmetro para **RpcStringBindingParse**. Isso faz com que a função ignore a análise do UUID do objeto. Como não analisa o UUID, **RpcStringBindingParse** não alocará uma cadeia de caracteres para ele. Essa técnica permite que seu aplicativo aloque apenas memória para as informações que você está interessado em analisar e analisar.

 

 




