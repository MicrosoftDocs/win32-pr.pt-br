---
title: Registrando pontos de extremidade
description: O registro do programa do servidor no mapa do ponto de extremidade do computador host do servidor permite que os programas cliente determinem qual ponto de extremidade (geralmente uma porta TCP/IP ou um pipe nomeado) o programa do servidor está escutando.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- Chamada de procedimento remoto RPC, tarefas, registrando pontos de extremidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6674d20eefa9ebd690f618c36f1dfe69f37dcf7743a0830e06cb38bc85ccfd56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926850"
---
# <a name="registering-endpoints"></a>Registrando pontos de extremidade

O registro do programa do servidor no mapa do ponto de extremidade do computador host do servidor permite que os programas cliente determinem qual ponto de extremidade (geralmente uma porta TCP/IP ou um pipe nomeado) o programa do servidor está escutando. Para se registrar no mapa de ponto de extremidade do sistema host do servidor, um programa de servidor chama a função [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) , conforme mostrado no fragmento de código a seguir:


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



O primeiro parâmetro para [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) é a estrutura que representa a interface. Você pode encontrá-lo no arquivo de cabeçalho que o compilador MIDL gerou do arquivo MIDL para esse aplicativo distribuído. Consulte [desenvolvendo a interface](developing-the-interface.md). Em seguida, **RpcEpRegister** precisa que seu aplicativo passe um conjunto de identificadores de ligação que são armazenados em um vetor de associação.

Além de registrar nomes de interface, o aplicativo de servidor também pode registrar UUIDs de objeto no mapa do ponto de extremidade. Neste exemplo, não há UUIDs de objeto para registrar, portanto, o terceiro parâmetro para [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) é definido como **NULL**.

O último parâmetro é uma cadeia de caracteres de comentário. Embora a biblioteca de tempo de execução RPC não use essa cadeia de caracteres, é recomendável definir a cadeia de caracteres, pois ela melhora a capacidade de gerenciamento do sistema. Um administrador do sistema pode usar a cadeia de caracteres para detectar quais portas são usadas por quais aplicativos, que podem ser usados para determinar quais portas serão gerenciadas por firewalls.

 

 




