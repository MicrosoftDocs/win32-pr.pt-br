---
title: Operações de conexão RAS
description: O Windows NT e versões posteriores fornecem as funções RasPhonebookDlg e RasDialDlg que exibem a interface do usuário interna para iniciar uma operação de conexão RAS.
ms.assetid: 1e0f82e1-5995-4b47-970b-e6a7ff6d52e0
keywords:
- Operações de conexão, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e2a78d34afd5aea3670730656e97886b6a5916
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823875"
---
# <a name="ras-connection-operations"></a>Operações de conexão RAS

O Windows NT e versões posteriores fornecem as funções [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) e [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) que exibem a interface do usuário interna para iniciar uma operação de conexão RAS. Para a maioria dos aplicativos, essa é a maneira preferida de iniciar uma operação de conexão RAS. No momento, o Windows 95 não oferece suporte a essas funções.

O restante desta seção descreve as funções de nível inferior para iniciar uma conexão RAS. Essas funções estão disponíveis no bothWindows NT 4,0 (e versões posteriores) e no Windows 95.

Um aplicativo cliente RAS usa a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para estabelecer uma conexão com um servidor RAS. A função **RasDial** inicia a operação de conexão, que é então executada pelo Gerenciador de conexões de acesso remoto.

O Gerenciador de conexões de acesso remoto é um serviço que manipula os detalhes do estabelecimento da conexão com o servidor remoto. Esse serviço também fornece ao cliente informações de status durante a operação de conexão. O Gerenciador de conexões de acesso remoto é iniciado automaticamente quando um aplicativo carrega o RASAPI32.DLL.

A chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especifica as seguintes informações ao iniciar uma operação de conexão:

-   As [informações de conexão](phone-book-files-and-connection-information.md) que o Gerenciador de conexões de acesso remoto precisa para estabelecer a conexão.
-   Um [manipulador de notificação](notification-handlers.md) opcional que recebe notificações de progresso durante a operação de conexão. Se a chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especificar um manipulador de notificação, a chamada será [assíncrona](asynchronous-operations.md); caso contrário, será [síncrono](synchronous-operations.md).
-   Uma estrutura opcional [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) para habilitar ou desabilitar extensões para a operação [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . As extensões permitem que um cliente RAS habilite diretamente algumas configurações de modem, para controlar se o RAS usa os prefixos e sufixos em uma entrada de catálogo telefônico e para dar suporte a [Estados pausados](paused-states.md) durante a operação de conexão.

 

 