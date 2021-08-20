---
description: Windows o WUA (agente de atualização) se atualiza automaticamente quando está conectado a um servidor Windows Server Update Services (WSUS) ou a Windows Update.
ms.assetid: 829112ab-b240-4cc4-8053-18b484934886
title: atualizando o agente de Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388475aaf9fa83413a916520035eb9539187390bf5a3bd8f5c836cb1b176357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814647"
---
# <a name="updating-windows-update-agent"></a>atualizando o agente de Windows Update

Windows o agente de atualização (WUA) é atualizado por meio de vários meios, dependendo da versão do Windows em execução no dispositivo. Versões antigas do WUA podem não ser capazes de se conectar aos serviços de atualização atuais, podem não ser compatíveis com todas as atualizações e podem não dar suporte a todas as APIs documentadas. Veja como garantir que o WUA seja totalmente atualizado e compatível.

**nas versões do Windows a partir do Windows 7 e do Windows Server 2008 R2**

Windows as atualizações do WUA (agente de atualização) estão incluídas nas atualizações periódicas regulares para Windows distribuídas por meio de Windows Update ou Windows Server Update Services WSUS). você não precisa realizar etapas especiais para atualizar o WUA nessas Windows versões.

**nas versões do Windows anteriores ao Windows 7 e Windows Server 2008 R2**

o WUA é atualizado automaticamente quando Atualizações Automáticas se conecta ao Windows Update ou ao WSUS.

se Atualizações Automáticas ainda não tiver sido executada com êxito, é possível que um dispositivo executando essas versões do Windows execute uma versão mais antiga do WUA que não ofereça suporte a todas as APIs documentadas. se você receber um resultado de WU_E_SELFUPDATE_REQUIRED ao usar a API do wua para executar uma verificação, download ou instalação, esse erro indicará que a versão instalada do WUA é muito antiga para se conectar aos serviços Windows Update atuais. Você não pode usar as APIs do WUA normal para atualizar o WUA nesses sistemas operacionais. 

um usuário pode atualizar o WUA manualmente para uma versão atual abrindo o painel de controle Windows Update, selecionando verificar se há atualizações e, em seguida, aceitando a autoatualização que aparece. Como alternativa, você pode atualizar o WUA programaticamente.

**para atualizar o WUA de forma programática em versões do Windows antes do Windows 7 e do Windows Server 2008 R2**

1.  Use as APIs do [WinHTTP](../winhttp/winhttp-start-page.md) para baixar [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
2.  Use as [funções de criptografia](../seccrypto/cryptography-functions.md) para verificar se a cópia baixada do [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab) tem uma assinatura digital da Microsoft. Se você não conseguir verificar a assinatura digital, pare.
3.  Use as APIs da [interface de descompactação de arquivo](../devnotes/cabinet-api-functions.md) para extrair o arquivo XML do [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
4.  Use as APIs de Microsoft XML Core Services ([MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85))) para carregar o arquivo XML e localizar o nó WURedist/StandaloneRedist/architecture para a arquitetura do computador. Por exemplo, para x86, localize o nó WURedist/StandaloneRedist/Architecture com o atributo **Name** de x86.
5.  Chame [**IWindowsUpdateAgentInfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) para determinar a versão atual do WUA. Se **IWindowsUpdateAgentInfo:: GetInfo** retornar um número de versão que seja pelo menos tão alto quanto o atributo **clientVersion** no nó de arquitetura que você localizou, pare.
6.  Use as APIs de [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) para ler o atributo **downloadUrl** do nó de arquitetura que você localizou. o **DownloadURL** fornece a URL de download para o instalador do WUA apropriado para a arquitetura do computador.
7.  Use as APIs do [WinHTTP](../winhttp/winhttp-start-page.md) para baixar o instalador apropriado.
8.  Use a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ou uma API semelhante para executar o instalador baixado.

 

 
