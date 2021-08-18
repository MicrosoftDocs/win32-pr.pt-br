---
title: Registrando a interface
description: Registrar a interface compatível com um programa de servidor permite que chamadas de procedimento remoto de programas cliente sejam expedidas para a rotina de servidor adequada.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, registrando a interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c444a82d30848f4f01643c08f17f484d027bc7b8c8efe3f10e7f3c194aac26a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926870"
---
# <a name="registering-the-interface"></a>Registrando a interface

Registrar a interface compatível com um programa de servidor permite que chamadas de procedimento remoto de programas cliente sejam expedidas para a rotina de servidor adequada. Os programas de servidor [**chamam RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para registrar suas interfaces. O fragmento de código a seguir demonstra seu uso:


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



O primeiro parâmetro para a função [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) é uma estrutura que o compilador MIDL gera do arquivo IDL que define a interface (ou interfaces) para o servidor. O segundo e o terceiro parâmetros são um UUID e um vetor de ponto de entrada, respectivamente. Eles são definidos como **NULL** neste exemplo. Em muitas instâncias, o programa de servidor definirá esses valores de parâmetro como **NULL.** Os programas de servidor usam o segundo e o terceiro parâmetros quando fornecem várias implementações dos mesmos procedimentos em uma interface. Para obter mais informações, consulte [Vetores de ponto de entrada](registering-interfaces.md).

Programas de servidor também podem usar [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) para registrar uma interface. Uma vantagem de usar essa função é que ela fornece ao seu aplicativo a capacidade de definir uma função de retorno de chamada de segurança. O uso de funções de retorno de chamada de segurança é a abordagem recomendada para proteger uma interface.

> [!Note]  
> MIDL produz duas estruturas muito semelhantes, uma para o cliente e outra para o servidor. A estrutura passada para a [**função RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) é a versão do servidor da estrutura produzida por MIDL.

 

 

 




