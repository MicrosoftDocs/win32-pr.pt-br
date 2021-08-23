---
description: O Windows de segurança permite controlar o acesso a objetos de evento, mutex, semáforo e temporizador de espera. Filas de temporizador, variáveis interlocked e objetos de seção críticos não sãocuráveis. Para obter mais informações, consulte Access-Control Modelo.
ms.assetid: 92478298-617c-4672-a1cc-9a8e9af40327
title: Segurança de objeto de sincronização e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85ca76002a92e305983ab97d46dfde2f36f9ae49a779e091a072d3090ceb976
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739286"
---
# <a name="synchronization-object-security-and-access-rights"></a>Segurança de objeto de sincronização e direitos de acesso

O Windows de segurança permite controlar o acesso a objetos de evento, mutex, semáforo e temporizador de espera. Filas de temporizador, variáveis interlocked e objetos de seção críticos não sãocuráveis. Para obter mais informações, consulte [Modelo de controle de acesso](../secauthz/access-control-model.md).

Você pode especificar um [descritor de](../secauthz/security-descriptors.md) segurança para um objeto de sincronização entre processos ao chamar a função [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex,**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)ou [**CreateWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) Se você especificar **NULL,** o objeto obtém um descritor de segurança padrão. As [ACLs (Listas](../secauthz/access-control-lists.md) de Controle de Acesso) no descritor de segurança padrão para um objeto de sincronização vêm do token primário ou de representação do criador.

Para obter ou definir o descritor de segurança de um objeto de temporizador de evento, mutex, semáforo ou waitable, chame as funções [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo,**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)ou [**SetSecurityInfo.**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo)

Os identificador retornados por [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex,**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)e [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) têm acesso completo ao novo objeto. Quando você chama as funções [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**OpenMutex,**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)e [**OpenWaitableTimer,**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) o sistema verifica os direitos de acesso solicitados no descritor de segurança do objeto.

Os direitos de acesso válidos para os objetos de sincronização entre processos incluem os [direitos de](../secauthz/standard-access-rights.md) acesso padrão e alguns direitos de acesso específicos do objeto. A tabela a seguir lista os direitos de acesso padrão usados por todos os objetos.

| Valor                           | Significado                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DELETE** (0x00010000L)        | Necessário para excluir o objeto .                                                                                                                                                                                                                                                           |
| **LEITURA \_ CONTROL** (0x00020000L) | Necessário para ler informações no descritor de segurança do objeto, não incluindo as informações na SACL. Para ler ou gravar a SACL, você deve solicitar o **direito de acesso ACCESS SYSTEM \_ \_ SECURITY.** Para obter mais informações, consulte [SACL Access Right](../secauthz/sacl-access-right.md). |
| **SYNCHRONIZE** (0x00100000L)   | O direito de usar o objeto para sincronização. Isso permite que um thread aguarde até que o objeto está no estado sinalizado.                                                                                                                                                                |
| **GRAVAÇÃO \_ DAC** (0x00040000L)    | Necessário para modificar a DACL no descritor de segurança para o objeto .                                                                                                                                                                                                                   |
| **GRAVAÇÃO \_ OWNER** (0x00080000L)  | Necessário para alterar o proprietário no descritor de segurança para o objeto .                                                                                                                                                                                                                  |



 

A tabela a seguir lista os direitos de acesso específicos do objeto para objetos de evento. Esses direitos têm suporte, além dos direitos de acesso padrão.



| Valor                             | Significado                                                                                                                                                                                                                                                                                          |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ ALL \_ ACCESS** (0x1F0003) | Todos os direitos de acesso possíveis para um objeto de evento. Use esse direito somente se seu aplicativo exigir acesso além do concedido pelos direitos de acesso padrão e **EVENT \_ MODIFY \_ STATE**. O uso desse direito de acesso aumenta a possibilidade de que seu aplicativo deve ser executado por um Administrador. |
| **EVENTO \_ MODIFY \_ STATE** (0x0002) | Modifique o acesso de estado, que é necessário para as funções [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent), [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) e [**PulseEvent.**](/windows/desktop/api/WinBase/nf-winbase-pulseevent)                                                                                                                                    |



 

A tabela a seguir lista os direitos de acesso específicos do objeto para objetos mutex. Esses direitos têm suporte, além dos direitos de acesso padrão.



| Valor                             | Significado                                                                                                                                                                                                                                                            |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MUTEX \_ ALL \_ ACCESS** (0x1F0001) | Todos os direitos de acesso possíveis para um objeto mutex. Use esse direito somente se seu aplicativo exigir acesso além do concedido pelos direitos de acesso padrão. O uso desse direito de acesso aumenta a possibilidade de que seu aplicativo deve ser executado por um Administrador. |
| **MUTEX \_ MODIFY \_ STATE** (0x0001) | Reservado para uso futuro.                                                                                                                                                                                                                                           |



 

A tabela a seguir lista os direitos de acesso específicos do objeto para objetos de semáforo. Esses direitos têm suporte, além dos direitos de acesso padrão.



| Valor                                 | Significado                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEMÁFORO \_ ALL \_ ACCESS** (0x1F0003) | Todos os direitos de acesso possíveis para um objeto de semáforo. Use esse direito somente se seu aplicativo exigir acesso além do concedido pelos direitos de acesso padrão e **SEMAPHORE \_ MODIFY \_ STATE**. O uso desse direito de acesso aumenta a possibilidade de que seu aplicativo deve ser executado por um Administrador. |
| **SEMÁFORO \_ MODIFY \_ STATE** (0x0002) | Modifique o acesso de estado, que é necessário para a [**função ReleaseSemaphore.**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore)                                                                                                                                                                                                   |



 

A tabela a seguir lista os direitos de acesso específicos do objeto para objetos de temporizador que podem ser aguardados. Esses direitos têm suporte, além dos direitos de acesso padrão.



| Valor                             | Significado                                                                                                                                                                                                                                                                                                  |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TIMER \_ ALL \_ ACCESS** (0x1F0003) | Todos os direitos de acesso possíveis para um objeto de temporizador que pode ser aguardado. Use esse direito somente se seu aplicativo exigir acesso além do concedido pelos direitos de acesso padrão e **TIMER \_ MODIFY \_ STATE**. O uso desse direito de acesso aumenta a possibilidade de que seu aplicativo deve ser executado por um Administrador. |
| **TIMER \_ MODIFY \_ STATE** (0x0002) | Modifique o acesso de estado, que é necessário para as funções [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) e [**CancelWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer)                                                                                                                                            |
| **TIMER \_ ESTADO DA \_ CONSULTA** (0x0001)  | Reservado para uso futuro.                                                                                                                                                                                                                                                                                 |



 

Para ler ou gravar a SACL de um objeto de sincronização entre processos, você deve solicitar o direito de acesso **ACCESS \_ SYSTEM \_ SECURITY.** Para obter mais informações, consulte [ACLs (Listas de Controle](../secauthz/access-control-lists.md) de Acesso) e [Direito de Acesso SACL.](../secauthz/sacl-access-right.md)

 

 
