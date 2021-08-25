---
title: Operações de conexão RAS
description: Windows NT e versões posteriores fornecem as funções RasPhonebookDlg e RasDialDlg que exibem a interface do usuário interna para iniciar uma operação de conexão RAS.
ms.assetid: 1e0f82e1-5995-4b47-970b-e6a7ff6d52e0
keywords:
- Operações de conexão, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e86ddf1586ce11f43e6b34ef15b89cb2d382b28911968f0b0f08dabd086a86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868456"
---
# <a name="ras-connection-operations"></a>Operações de conexão RAS

Windows NT e versões posteriores fornecem as funções [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) e [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) que exibem a interface do usuário interna para iniciar uma operação de conexão RAS. Para a maioria dos aplicativos, essa é a maneira preferencial de iniciar uma operação de conexão RAS. Windows 95 atualmente não dá suporte a essas funções.

O restante desta seção descreve as funções de baixo nível para iniciar uma conexão RAS. Essas funções estão disponíveis noWindows NT 4.0 (e versões posteriores) e Windows 95.

Um aplicativo cliente RAS usa a [**função RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para estabelecer uma conexão com um servidor RAS. A **função RasDial** inicia a operação de conexão, que é executada pela Gerenciador de Conexões.

O Gerenciador de Conexões remoto é um serviço que lida com os detalhes do estabelecimento da conexão com o servidor remoto. Esse serviço também fornece ao cliente informações de status durante a operação de conexão. O controle de Gerenciador de Conexões remoto é iniciado automaticamente quando um aplicativo carrega o RASAPI32.DLL.

A [**chamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especifica as seguintes informações ao iniciar uma operação de conexão:

-   As [informações de conexão](phone-book-files-and-connection-information.md) que o Gerenciador de Conexões remoto precisa para estabelecer a conexão.
-   Um manipulador [de notificação opcional](notification-handlers.md) que recebe notificações de progresso durante a operação de conexão. Se a [**chamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especificar um manipulador de notificação, a chamada será [assíncrona](asynchronous-operations.md); caso contrário, será [síncrono.](synchronous-operations.md)
-   Uma estrutura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) opcional para habilitar ou desabilitar extensões para a [**operação RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala) As extensões permitem que um cliente RAS habilita diretamente algumas configurações de modem, para controlar se [](paused-states.md) o RAS usa os prefixos e sufixos em uma entrada de phone-book e para dar suporte a estados em pausa durante a operação de conexão.

 

 