---
title: Monitorando conexões de sessão e desconexões
description: Para registrar um aplicativo com Serviços de Área de Trabalho Remota, armazene o nome do aplicativo de servidor do virtual Channel no registro adicionando uma subchave.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007652"
---
# <a name="monitoring-session-connections-and-disconnections"></a>Monitorando conexões de sessão e desconexões

Para um aplicativo de serviço, como um aplicativo de servidor de canal virtual, para monitorar conexões de sessão e desconexões, você deve registrá-lo com Serviços de Área de Trabalho Remota. Para registrar o aplicativo com Serviços de Área de Trabalho Remota, armazene o nome do aplicativo de servidor do virtual Channel no registro adicionando uma subchave no seguinte local:

**HKEY \_ O sistema de \_ computador local** \\  \\ **CurrentControlSet** \\ **Control** \\ **TerminalServer** \\ **AddIns**

A subchave pode ter qualquer nome. Ele deve ter um valor de **reg \_ sz** , **nome**, que contenha o nome simbólico do aplicativo.

``` syntax
Name = AddinName
```

O comprimento máximo da subchave e do valor do **nome** é de 99 caracteres.

A subchave também deve ter um valor **reg \_ DWORD** que indica o tipo de aplicativo de servidor.

``` syntax
Type = AddinType
```

*Addintype* deve ser o valor a seguir.



| Valor | Significado                               |
|-------|---------------------------------------|
| 3     | Aplicativo de modo de usuário, espaço de sessão. |



 

O registro do aplicativo de serviço entra em vigor somente em sessões criadas após a execução do registro.

Para cada aplicativo de serviço registrado, Serviços de Área de Trabalho Remota sinalizará um conjunto de objetos de evento quando um cliente se conectar ou se desconectar da sessão. Cada plug-in de canal virtual deve se registrar e criar os eventos de notificação chamando [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa). Os nomes desses objetos de evento aderem ao formato a seguir.

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

*AddInName* é a cadeia de caracteres especificada no valor de **nome** da subchave do registro sob a qual o aplicativo do servidor está registrado. A criação desses eventos em uma sessão faz com que eles sejam criados em um diretório de eventos por sessão especial. O diretório de eventos fornece segurança adicional, impedindo que aplicativos em outras sessões modifiquem o estado desses eventos.

Para controlar se os eventos reconectar e desconectar são recebidos no servidor, você pode posicionar o sinalizador **RemoteControlPersistent** no registro na seguinte chave:

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **controle** \\ **TerminalServer** \\ **AddIns** \\ *AddInName*

O sinalizador habilita ou desabilita a reconexão e a desconexão de eventos de serem sinalizados quando uma sessão de cliente é iniciada ou interrompida. A sintaxe do valor de **reg \_ DWORD** é a seguinte.

``` syntax
RemoteControlPersistent = flag
```

O valor do *sinalizador* pode ser um ou zero. Zero é o valor padrão. Se definido como um, o aplicativo de serviço não será notificado se a sessão do cliente for iniciada ou interrompida. Se definido como zero, um evento reconnect será sinalizado quando a sessão do cliente for iniciada e um evento de desconexão será sinalizado quando a sessão do cliente for interrompida.

O formato de nome de objeto de evento anterior ainda tem suporte no Windows Server 2008 para compatibilidade com versões anteriores. É recomendável que você use o formato mais recente do Windows Server 2008, pois ele é mais seguro.

O formato de evento anterior é o seguinte.

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

*AddInName* é a cadeia de caracteres especificada no valor de **nome** da subchave do registro sob a qual o aplicativo do servidor está registrado. *SessionID* é o identificador de sessão de uma sessão de cliente.

 

 