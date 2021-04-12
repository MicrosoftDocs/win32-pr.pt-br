---
title: Transação de autenticação de DLL de segurança RAS
description: O servidor RAS do Windows NT/Windows 2000 chama a função RasSecurityDialogBegin da DLL de segurança para iniciar uma autenticação de um usuário remoto.
ms.assetid: e6549812-d906-4163-b9c8-86f8f1cb1ad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109f6ad5cd3d7b76e30db099a478ffaf562feb32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499129"
---
# <a name="ras-security-dll-authentication-transaction"></a>Transação de autenticação de DLL de segurança RAS

O servidor RAS do Windows NT/Windows 2000 chama a função [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) da DLL de segurança para iniciar uma autenticação de um usuário remoto. O servidor RAS está bloqueado e não pode aceitar nenhuma outra chamada até que **RasSecurityDialogBegin** seja retornado. Por esse motivo, **RasSecurityDialogBegin** deve copiar os parâmetros de entrada, criar um thread para executar a autenticação e retornar o mais rápido possível.

O thread criado pela DLL de segurança usa as funções [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) e [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) para se comunicar com o computador remoto. Essas funções não estão disponíveis para importação estática de qualquer biblioteca. Em vez disso, a DLL de segurança deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a essas funções no RASMAN.DLL.

Durante uma transação de autenticação, o Gerenciador de conexões RAS no computador remoto exibe uma janela de terminal. O thread da DLL de segurança chama [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) para enviar uma mensagem a ser exibida na janela do terminal. Em seguida, o thread chama [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) para receber a entrada que o usuário remoto digita na janela do terminal. O thread pode fazer qualquer número de chamadas **RasSecurityDialogSend** , com cada chamada seguida de uma chamada **RasSecurityDialogReceive** . Após cada chamada para **RasSecurityDialogReceive**, o thread deve chamar uma das funções Wait, como [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), para aguardar a conclusão das operações de envio e recebimento assíncronas. O servidor RAS sinaliza um objeto de evento quando a operação de recebimento tiver sido concluída ou quando um intervalo de tempo limite opcional tiver decorrido.

Quando o thread terminar de autenticar o usuário remoto, ele chamará a função [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) . Essa chamada passa uma estrutura de [**\_ mensagem de segurança**](/windows/desktop/api/Rasshost/ns-rasshost-security_message) que contém os resultados da transação de autenticação para o servidor RAS. Em seguida, o servidor RAS executa uma sequência de limpeza que inclui uma chamada para a função [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) da dll. Isso dá à DLL de segurança uma oportunidade de executar qualquer limpeza necessária.

A DLL de segurança pode chamar a função [**RasSecurityDialogGetInfo**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialoggetinfo) para recuperar informações sobre a porta associada a uma transação de autenticação. **RasSecurityDialogGetInfo** preenche uma estrutura [**de \_ \_ informações de segurança de Ras**](/windows/desktop/api/Rasshost/ns-rasshost-ras_security_info) que indica o estado da última chamada de [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) para a porta.

 

 