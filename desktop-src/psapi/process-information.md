---
title: Informações do processo
description: O sistema mantém uma lista de processos em execução. Você pode recuperar os identificadores para esses processos chamando a função EnumProcesses. Essa função preenche uma matriz de valores DWORD com os identificadores de todos os processos no sistema.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294199"
---
# <a name="process-information"></a>Informações do processo

O sistema mantém uma lista de processos em execução. Você pode recuperar os identificadores para esses processos chamando a função [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Essa função preenche uma matriz de valores **DWORD** com os identificadores de todos os processos no sistema.

Muitas funções no PSAPI exigem um identificador de processo. Para obter um identificador de processo para um processo em execução, passe seu identificador de processo (obtido de [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) para a função [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) . Lembre-se de chamar a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) quando terminar com o identificador de processo.

 

 