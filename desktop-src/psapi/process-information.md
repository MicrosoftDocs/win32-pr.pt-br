---
title: Informações do processo
description: O sistema mantém uma lista de processos em execução. Você pode recuperar os identificadores desses processos chamando a função EnumProcesses. Essa função preenche uma matriz de valores DWORD com os identificadores de todos os processos no sistema.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5facb72f094059997c271cb9f38beaea08981430bba40902d620a23e2875b26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094887"
---
# <a name="process-information"></a>Informações do processo

O sistema mantém uma lista de processos em execução. Você pode recuperar os identificadores desses processos chamando a [**função EnumProcesses.**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) Essa função preenche uma matriz de **valores DWORD** com os identificadores de todos os processos no sistema.

Muitas funções no PSAPI exigem um alçamento de processo. Para obter um identificador de processo para um processo em execução, passe seu identificador de processo (obtido de [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) para a [**função OpenProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) Lembre-se de chamar [**a função CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) quando terminar de usar o handle do processo.

 

 