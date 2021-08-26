---
description: Todos os usuários têm acesso de leitura à lista de processos no sistema e há várias funções diferentes que enumeram os processos ativos. A função que você deve usar dependerá de fatores como o suporte à plataforma desejada.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Enumeração de processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05caa13d0f53fc87828669b2e19eba126c62c28f492b2f41d09caf2377321a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081316"
---
# <a name="process-enumeration"></a>Enumeração de processo

Todos os usuários têm acesso de leitura à lista de processos no sistema e há várias funções diferentes que enumeram os processos ativos. A função que você deve usar dependerá de fatores como o suporte à plataforma desejada.

As funções a seguir são usadas para enumerar processos.



| Função                                                    | Descrição                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Recupera o identificador de processo para cada objeto de processo no sistema.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Recupera informações sobre o primeiro processo encontrado em um instantâneo do sistema.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Recupera informações sobre o próximo processo registrado em um instantâneo do sistema.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Recupera informações sobre os processos ativos no servidor terminal especificado. |



 

As funções toolhelp [**e EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumeram todo o processo. Para listar os processos em execução em uma conta de usuário específica, use [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) e filtre o SID do usuário. Você pode filtrar a ID da sessão para ocultar processos em execução em outras sessões do servidor terminal.

Você também pode filtrar processos por conta de usuário, independentemente da função de enumeração, chamando [**OpenProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)e [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) com **TokenUser**. No entanto, você não pode abrir um processo protegido por um descritor de segurança, a menos que você tenha acesso concedido.

 

 
