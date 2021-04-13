---
description: Um direito de acesso é um sinalizador de bit que corresponde a um determinado conjunto de operações que um thread pode executar em um objeto protegível.
ms.assetid: da67c486-d2e7-4632-ac7a-c18aabc3f21d
title: Direitos de acesso e máscaras de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f06cdf447f9d91c1553ea5fb6b3b7d1f324dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370719"
---
# <a name="access-rights-and-access-masks"></a>Direitos de acesso e máscaras de acesso

Um *direito de acesso* é um sinalizador de bit que corresponde a um determinado conjunto de operações que um thread pode executar em um objeto protegível. Por exemplo, uma chave do registro tem o \_ direito de acesso ao valor do conjunto de chaves \_ , que corresponde à capacidade de um thread definir um valor sob a chave. Se um thread tentar executar uma operação em um objeto, mas não tiver o direito de acesso necessário ao objeto, o sistema não executará a operação.

Uma [*máscara de acesso*](/windows/desktop/SecGloss/a-gly) é um valor de 32 bits cujos bits correspondem aos direitos de acesso com suporte de um objeto. Todos os objetos protegíveis do Windows usam um [formato de máscara de acesso](access-mask-format.md) que inclui bits para os seguintes tipos de direitos de acesso:

-   [Direitos de acesso genéricos](generic-access-rights.md)
-   [Direitos de acesso padrão](standard-access-rights.md)
-   [Direito de acesso à SACL](sacl-access-right.md)
-   [Direitos de acesso aos serviços de diretório](directory-services-access-rights.md)

Quando um thread tenta abrir um identificador para um objeto, o thread normalmente especifica uma máscara de acesso para [solicitar um conjunto de direitos de acesso](requesting-access-rights-to-an-object.md). Por exemplo, um aplicativo que precisa definir e consultar os valores de uma chave do registro pode abrir a chave usando uma máscara de acesso para solicitar o valor do conjunto de chaves \_ e os direitos de acesso do valor da consulta de \_ chave \_ \_ .

A tabela a seguir mostra as funções que manipulam as informações de segurança para cada tipo de objeto protegível.



| Tipo de objeto                                                                                                                                           | Funções de descritor de segurança                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Arquivos ou diretórios](/windows/desktop/FileIO/file-security-and-access-rights) em um sistema de arquivos NTFS                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Pipes anônimos](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights) de [pipes nomeados](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/>                 | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| Buffers da tela do console                                                                                                                                | Não há suporte.                                                                                                                                                                                     |
| [Processa](/windows/desktop/ProcThread/process-security-and-access-rights)[threads](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                                      | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Objetos de mapeamento de arquivos](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Tokens de acesso](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Objetos de gerenciamento de janelas ([estações de janela](/windows/desktop/winstation/window-station-security-and-access-rights) e áreas de [trabalho](/windows/desktop/winstation/desktop-security-and-access-rights)) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Chaves do Registro](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Serviços do Windows](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Impressoras locais ou remotas                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Compartilhamentos de rede                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objetos de sincronização entre processos](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (eventos, mutexes, semáforos e temporizadores de espera)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objetos de trabalho](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |



 

 

