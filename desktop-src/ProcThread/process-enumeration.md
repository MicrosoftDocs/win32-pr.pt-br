---
description: Todos os usuários têm acesso de leitura à lista de processos no sistema e há várias funções diferentes que enumeram os processos ativos. A função que você deve usar dependerá de fatores como o suporte à plataforma desejada.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Enumeração de processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758730"
---
# <a name="process-enumeration"></a>Enumeração de processo

Todos os usuários têm acesso de leitura à lista de processos no sistema e há várias funções diferentes que enumeram os processos ativos. A função que você deve usar dependerá de fatores como o suporte à plataforma desejada.

As funções a seguir são usadas para enumerar processos.



| Função                                                    | Descrição                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Recupera o identificador de processo para cada objeto de processo no sistema.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Recupera informações sobre o primeiro processo encontrado em um instantâneo do sistema.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Recupera informações sobre o próximo processo registrado em um instantâneo do sistema.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Recupera informações sobre os processos ativos no servidor de terminal especificado. |



 

O ToolHelp funções e [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumeram todos os processos. Para listar os processos que estão sendo executados em uma conta de usuário específica, use [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) e filtre no SID do usuário. Você pode filtrar a ID da sessão para ocultar os processos em execução em outras sessões do Terminal Server.

Você também pode filtrar processos por conta de usuário, independentemente da função de enumeração, chamando [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)e [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) com **TokenUser**. No entanto, você não pode abrir um processo protegido por um descritor de segurança, a menos que tenha recebido acesso.

 

 
