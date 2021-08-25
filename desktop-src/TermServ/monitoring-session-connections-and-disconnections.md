---
title: Monitoramento de conexões de sessão e desconexões
description: Para registrar um aplicativo com Serviços de Área de Trabalho Remota, armazene o nome do aplicativo de servidor de canal virtual no Registro adicionando uma sub-chave.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2813399650d535d10864f384afb6b745fb9e50039f2b981df61ceb2e6452a608
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989096"
---
# <a name="monitoring-session-connections-and-disconnections"></a>Monitoramento de conexões de sessão e desconexões

Para um aplicativo de serviço, como um aplicativo de servidor de canal virtual, para monitorar conexões de sessão e desconexões, você deve registrá-lo com Serviços de Área de Trabalho Remota. Para registrar o aplicativo com Serviços de Área de Trabalho Remota, armazene o nome do aplicativo de servidor de canal virtual no Registro adicionando uma sub-chave no seguinte local:

**HKEY \_ Terminal \_ do controle CurrentControlSet** do sistema \\  \\ **LOCAL** \\  \\ **MACHINEServer** \\ **Addins**

A sub-chave pode ter qualquer nome. Ele deve ter um **valor \_ REG SZ,** **Name**, que contém o nome simbólico do aplicativo.

``` syntax
Name = AddinName
```

O comprimento máximo da sub-chave e do valor de **Name** é de 99 caracteres.

A sub-chave também deve ter **um valor REG \_ DWORD** que indica o tipo de aplicativo de servidor.

``` syntax
Type = AddinType
```

*AddinType* deve ser o valor a seguir.



| Valor | Significado                               |
|-------|---------------------------------------|
| 3     | Aplicativo de modo de usuário, espaço de sessão. |



 

O registro do aplicativo de serviço entra em vigor somente em sessões criadas depois que o registro foi executado.

Para cada aplicativo de serviço registrado, Serviços de Área de Trabalho Remota sinaliza um conjunto de objetos de evento quando um cliente se conecta ou se desconecta da sessão. Cada plug-in de canal virtual deve se registrar e criar os eventos de notificação chamando [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa). Os nomes desses objetos de evento seguem o formato a seguir.

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

*AddinName* é a cadeia de caracteres especificada no valor **Nome** da sub-chave do Registro na qual o aplicativo do servidor está registrado. A criação desses eventos em uma sessão faz com que eles sejam criados em um diretório de eventos especial por sessão. O diretório de eventos fornece segurança adicionada, impedindo que aplicativos em outras sessões modifiquem o estado desses eventos.

Para controlar se os eventos RECONNECT e DISCONNECT são recebidos no servidor, você pode colocar o sinalizador **RemoteControlPersistent** no Registro sob a seguinte chave:

**HKEY \_ Terminal \_ do** \\  \\ **controle CurrentControlSet** do sistema LOCAL \\  \\ **MACHINEServer** \\  \\ *Addins addinname*

O sinalizador permite ou desabilita a sinalização de eventos RECONNECT e DISCONNECT quando uma sessão do cliente é iniciada ou interrompida. A sintaxe do valor **\_ REG DWORD** é a seguinte.

``` syntax
RemoteControlPersistent = flag
```

O valor do *sinalizador* pode ser um ou zero. Zero é o valor padrão. Se definido como um, o aplicativo de serviço não será notificado se a sessão do cliente for iniciada ou interrompida. Se definido como zero, um evento RECONNECT será sinalizado quando a sessão do cliente for iniciada e um evento DISCONNECT será sinalizado quando a sessão do cliente for interrompida.

O formato de nome do objeto de evento anterior ainda tem suporte no Windows Server 2008 para compatibilidade com versões anteriores. É recomendável que você use o formato Windows Server 2008 mais novo porque ele é mais seguro.

O formato de evento anterior é o seguinte.

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

*AddinName* é a cadeia de caracteres especificada no valor **Nome** da sub-chave do Registro na qual o aplicativo do servidor está registrado. *SessionId* é o identificador de sessão de uma sessão do cliente.

 

 