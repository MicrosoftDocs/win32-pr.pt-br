---
title: Registrando a interface
description: Registrar a interface que um programa de servidor dá suporte permite que chamadas de procedimento remotos de programas cliente sejam expedidas para a rotina de servidor adequada.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- Chamada de procedimento remoto RPC, tarefas, registrando a interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159288"
---
# <a name="registering-the-interface"></a>Registrando a interface

Registrar a interface que um programa de servidor dá suporte permite que chamadas de procedimento remotos de programas cliente sejam expedidas para a rotina de servidor adequada. Os programas de servidor chamam [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para registrar suas interfaces. O fragmento de código a seguir demonstra seu uso:


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



O primeiro parâmetro para a função [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) é uma estrutura que o compilador MIDL gera a partir do arquivo IDL que define a interface (ou interfaces) para o servidor. O segundo e o terceiro parâmetros são um UUID e um vetor de ponto de entrada, respectivamente. Eles são definidos como **NULL** neste exemplo. Em muitos casos, o programa do servidor definirá esses valores de parâmetro como **NULL**. Os programas de servidor usam o segundo e o terceiro parâmetros quando fornecem várias implementações dos mesmos procedimentos em uma interface. Para obter mais informações, consulte [vetores de ponto de entrada](registering-interfaces.md).

Os programas de servidor também podem usar o [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) para registrar uma interface. Uma vantagem de usar essa função é que ela fornece ao aplicativo a capacidade de definir uma função de retorno de chamada de segurança. O uso de funções de retorno de chamada de segurança é a abordagem recomendada para proteger uma interface.

> [!Note]  
> O MIDL produz duas estruturas muito semelhantes, uma para o cliente e outra para o servidor. A estrutura passada para a função [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) é a versão do servidor da estrutura gerada pelo MIDL.

 

 

 




