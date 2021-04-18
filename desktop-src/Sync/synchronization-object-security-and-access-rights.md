---
description: O modelo de segurança do Windows permite que você controle o acesso a objetos de timer de evento, mutex, semáforo e esperados. Filas de temporizador, variáveis interbloqueadas e objetos de seção crítica não são protegíveis. Para obter mais informações, consulte modelo de Access-Control.
ms.assetid: 92478298-617c-4672-a1cc-9a8e9af40327
title: Segurança do objeto de sincronização e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c4bfdb17a6e1c4d99a3e9722e67a3b48a3c788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756130"
---
# <a name="synchronization-object-security-and-access-rights"></a>Segurança do objeto de sincronização e direitos de acesso

O modelo de segurança do Windows permite que você controle o acesso a objetos de timer de evento, mutex, semáforo e esperados. Filas de temporizador, variáveis interbloqueadas e objetos de seção crítica não são protegíveis. Para obter mais informações, consulte [modelo de controle de acesso](../secauthz/access-control-model.md).

Você pode especificar um [descritor de segurança](../secauthz/security-descriptors.md) para um objeto de sincronização entre processos ao chamar a função [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**createsemáforo**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)ou [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) . Se você especificar **NULL**, o objeto obterá um descritor de segurança padrão. As [listas de controle de acesso (ACLs)](../secauthz/access-control-lists.md) no descritor de segurança padrão para um objeto de sincronização são provenientes do token principal ou de representação do criador.

Para obter ou definir o descritor de segurança de um objeto de evento, mutex, Semaphore ou timer de espera, chame as funções [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)ou [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

Os identificadores retornados por [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**createsemáforo**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)e [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) têm acesso completo ao novo objeto. Quando você chama as funções [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw), [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)e [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) , o sistema verifica os direitos de acesso solicitados no descritor de segurança do objeto.

Os direitos de acesso válidos para os objetos de sincronização entre processos incluem os [direitos de acesso padrão](../secauthz/standard-access-rights.md) e alguns direitos de acesso específicos ao objeto. A tabela a seguir lista os direitos de acesso padrão usados por todos os objetos.

| Valor                           | Significado                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Excluir** (0x00010000L)        | Necessário para excluir o objeto.                                                                                                                                                                                                                                                           |
| **Ler \_ CONTROL** (0x00020000L) | Necessário para ler informações no descritor de segurança do objeto, não incluindo as informações na SACL. Para ler ou gravar a SACL, você deve solicitar o direito de acesso de **\_ \_ segurança do sistema de acesso** . Para obter mais informações, consulte [direitos de acesso à SACL](../secauthz/sacl-access-right.md). |
| **Sincronizar** (0x00100000L)   | O direito de usar o objeto para sincronização. Isso permite que um thread aguarde até que o objeto esteja no estado sinalizado.                                                                                                                                                                |
| **Gravar \_ DAC** (0x00040000L)    | Necessário para modificar a DACL no descritor de segurança do objeto.                                                                                                                                                                                                                   |
| **Gravar \_ PROPRIETÁRIO** (0x00080000L)  | Necessário para alterar o proprietário no descritor de segurança do objeto.                                                                                                                                                                                                                  |



 

A tabela a seguir lista os direitos de acesso específicos ao objeto para objetos de evento. Esses direitos têm suporte além dos direitos de acesso padrão.



| Valor                             | Significado                                                                                                                                                                                                                                                                                          |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Todos os \_ acessos** (0x1F0003) | Todos os direitos de acesso possíveis para um objeto de evento. Use este direito somente se seu aplicativo exigir acesso além daquele concedido pelo **\_ \_ estado de modificação de eventos** e direitos de acesso padrão. Usar esse direito de acesso aumenta a possibilidade de o aplicativo ser executado por um administrador. |
| **Evento \_ de MODIFICAR \_ estado** (0x0002) | Modifique o acesso ao estado, que é necessário para as funções [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent), [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) e [**PulseEvent**](/windows/desktop/api/WinBase/nf-winbase-pulseevent) .                                                                                                                                    |



 

A tabela a seguir lista os direitos de acesso específicos ao objeto para objetos mutex. Esses direitos têm suporte além dos direitos de acesso padrão.



| Valor                             | Significado                                                                                                                                                                                                                                                            |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mutex \_ Todos os \_ acessos** (0x1F0001) | Todos os direitos de acesso possíveis para um objeto mutex. Use este direito somente se seu aplicativo exigir acesso além daquele concedido pelos direitos de acesso padrão. Usar esse direito de acesso aumenta a possibilidade de o aplicativo ser executado por um administrador. |
| **Mutex \_ MODIFICAR \_ estado** (0x0001) | Reservado para uso futuro.                                                                                                                                                                                                                                           |



 

A tabela a seguir lista os direitos de acesso específicos ao objeto para objetos Semaphore. Esses direitos têm suporte além dos direitos de acesso padrão.



| Valor                                 | Significado                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Semáforo \_ Todos os \_ acessos** (0x1F0003) | Todos os direitos de acesso possíveis para um objeto Semaphore. Use este direito somente se seu aplicativo exigir acesso além daquele concedido pelo **\_ \_ estado de modificação de semáforo** e direitos de acesso padrão. Usar esse direito de acesso aumenta a possibilidade de o aplicativo ser executado por um administrador. |
| **Semáforo \_ MODIFICAR \_ estado** (0x0002) | Modifique o acesso ao estado, que é necessário para a função [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) .                                                                                                                                                                                                   |



 

A tabela a seguir lista os direitos de acesso específicos ao objeto para objetos de timer que esperam. Esses direitos têm suporte além dos direitos de acesso padrão.



| Valor                             | Significado                                                                                                                                                                                                                                                                                                  |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Temporizador \_ Todos os \_ acessos** (0x1F0003) | Todos os direitos de acesso possíveis para um objeto de temporizador que pode ser aguardado. Use este direito somente se seu aplicativo exigir acesso além daquele concedido pelo **\_ \_ estado de modificação** de direitos de acesso e do temporizador padrão. Usar esse direito de acesso aumenta a possibilidade de o aplicativo ser executado por um administrador. |
| **Temporizador \_ MODIFICAR \_ estado** (0x0002) | Modifique o acesso ao estado, que é necessário para as funções [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) e [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) .                                                                                                                                            |
| **Temporizador \_ \_Estado da consulta** (0x0001)  | Reservado para uso futuro.                                                                                                                                                                                                                                                                                 |



 

Para ler ou gravar a SACL de um objeto de sincronização entre processos, você deve solicitar o direito de acesso de **\_ \_ segurança do sistema de acesso** . Para obter mais informações, consulte [listas de controle de acesso (ACLs)](../secauthz/access-control-lists.md) e [direito de acesso SACL](../secauthz/sacl-access-right.md).

 

 
