---
title: Recuperação de aplicativo e funções de reinicialização
description: Recuperação e reinicialização do aplicativo define as funções a seguir
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084741"
---
# <a name="application-recovery-and-restart-functions"></a>Recuperação de aplicativo e funções de reinicialização

A recuperação e a reinicialização do aplicativo define as seguintes funções:



| Função                                                                               | Descrição                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**ApplicationRecoveryFinished**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | Indica que o aplicativo de chamada concluiu sua recuperação de dados.                    |
| [**ApplicationRecoveryInProgress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | Indica que o aplicativo de chamada está continuando a recuperar dados.                      |
| [**GetApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | Recupera um ponteiro para a rotina de retorno de chamada de recuperação registrada para o processo especificado. |
| [**GetApplicationRestartSettings**](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | Recupera as informações de reinicialização registradas para o processo especificado.                    |
| [**RegisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | Registra a instância ativa de um aplicativo para recuperação.                              |
| [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | Registra a instância ativa de um aplicativo para reinicializar.                               |
| [**UnregisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | Remove a instância ativa de um aplicativo da lista de recuperação.                      |
| [**UnregisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | Remove a instância ativa de um aplicativo da lista de reinicialização.                       |



 

 

 