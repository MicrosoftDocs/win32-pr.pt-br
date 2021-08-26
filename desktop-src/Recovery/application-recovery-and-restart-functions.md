---
title: Funções de recuperação e reinicialização de aplicativos
description: A Recuperação e Reinicialização de Aplicativos define as seguintes funções
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df0a2139a24c3e69ae328533d6bf8b1baeee2043bc82b9f8d50f4272a16e2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024616"
---
# <a name="application-recovery-and-restart-functions"></a>Funções de recuperação e reinicialização de aplicativos

A Recuperação e Reinicialização de Aplicativos define as seguintes funções:



| Função                                                                               | Descrição                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**ApplicationRecoveryFinished**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | Indica que o aplicativo de chamada concluiu sua recuperação de dados.                    |
| [**ApplicationRecoveryInProgress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | Indica que o aplicativo de chamada continua a recuperar dados.                      |
| [**GetApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | Recupera um ponteiro para a rotina de retorno de chamada de recuperação registrada para o processo especificado. |
| [**GetApplicationRestartSettings**](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | Recupera as informações de reinicialização registradas para o processo especificado.                    |
| [**RegisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | Registra a instância ativa de um aplicativo para recuperação.                              |
| [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | Registra a instância ativa de um aplicativo para reinicialização.                               |
| [**UnregisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | Remove a instância ativa de um aplicativo da lista de recuperação.                      |
| [**UnregisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | Remove a instância ativa de um aplicativo da lista de reinicialização.                       |



 

 

 