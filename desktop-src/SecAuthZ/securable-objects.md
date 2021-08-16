---
description: Um objeto seguro é um objeto que pode ter um descritor de segurança.
ms.assetid: 32f2ec06-822f-4d1e-bf51-5ae1d7355e60
title: Objetos que podem sercuráveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93af0153082a5e94577e96e3b3f85c30ced8775aa8617bff84db37c96904d814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780501"
---
# <a name="securable-objects"></a>Objetos que podem sercuráveis

Um objeto seguro é um objeto que pode ter um [descritor de segurança](security-descriptors.md). Todos os Windows objetos nomeados sãocuráveis. Alguns objetos sem nome, como [*objetos de processo*](/windows/desktop/SecGloss/p-gly) e thread, também podem ter descritores de segurança. Para a maioria dos objetos de segurança, você pode especificar o [*descritor de*](/windows/desktop/SecGloss/s-gly) segurança de um objeto na chamada de função que cria o objeto . Por exemplo, você pode especificar um descritor de segurança nas [**funções CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

Além disso, as Windows de segurança permitem obter e definir as informações de segurança para objetos securáveis criados em sistemas operacionais diferentes Windows. As Windows de segurança também oferecem suporte para usar descritores de segurança com objetos particulares definidos pelo aplicativo. Para obter mais informações sobre objetos de segurança privados, consulte [Controle de acesso de cliente/servidor](client-server-access-control.md).

Cada tipo de objetocurável define seu [](access-rights-and-access-masks.md) próprio conjunto de direitos de acesso específicos e seu próprio [mapeamento de direitos de acesso genéricos.](generic-access-rights.md) Para obter informações sobre os direitos de acesso específicos e genéricos para cada tipo de objeto securável, consulte a visão geral desse tipo de objeto.

A tabela a seguir mostra as funções a ser usadas para manipular as informações de segurança de alguns objetos que podem sercuráveis comuns.



| Tipo de objeto                                                                                                                                           | Funções do descritor de segurança                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Arquivos ou diretórios](/windows/desktop/FileIO/file-security-and-access-rights) em um sistema de arquivos NTFS                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Pipes nomeados](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/> [Pipes anônimos](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>     | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Processos](/windows/desktop/ProcThread/process-security-and-access-rights)<br/> [Threads](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                          | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Objetos de mapeamento de arquivo](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Tokens de acesso](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Objetos de gerenciamento de janelas[(estações de janela e](/windows/desktop/winstation/window-station-security-and-access-rights) [áreas de trabalho)](/windows/desktop/winstation/desktop-security-and-access-rights) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Chaves do Registro](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Serviços Windows](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Impressoras locais ou remotas                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Compartilhamentos de rede                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objetos de sincronização entre processos](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (eventos, mutexes, semáforos e temporizadores de espera)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objetos de trabalho](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Objetos de serviço de diretório                                                                                                                             | Esses objetos são manipulados por Objetos do Active Directory. Para obter mais informações, consulte [Interfaces de serviço do Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).                             |



 

 

