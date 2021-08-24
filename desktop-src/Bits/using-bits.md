---
title: Usando BITS
description: Usando BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- BITS
- Serviço de Transferência Inteligente em Segundo Plano, tarefas
- BITS de transferência de arquivo
- Usando BITS BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b301c1d96956bca924d99ef41ade3032f58dc4e194b420069cbae1071c916b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801156"
---
# <a name="using-bits"></a>Usando BITS

As etapas a seguir mostram como executar uma transferência de arquivo usando as  [interfaces](bits-interfaces.md)Serviço de Transferência Inteligente em Segundo Plano (BITS).

**Para executar uma transferência de arquivo**

1.  [Conexão para o serviço BITS](connecting-to-the-bits-service.md)
2.  [Criar um trabalho de transferência](creating-a-job.md)
3.  [Adicionar arquivos ao trabalho](adding-files-to-a-job.md)
4.  [Iniciar o trabalho](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [Determinar se o BITS transferiu os arquivos com êxito](determining-the-status-of-a-job.md)
6.  [Concluir o trabalho](completing-and-canceling-a-job.md)

As etapas anteriores mostram como transferir arquivos usando os valores de propriedade padrão para um trabalho. Você pode alterar o comportamento padrão alterando um ou mais dos valores de propriedade do trabalho. Por exemplo, você pode alterar a prioridade de que o trabalho é processado em relação a outros trabalhos na fila, especificar sua própria configuração de proxy e registrar-se para receber a notificação de eventos quando o BITS tiver transferido os arquivos. Para obter mais informações, [consulte Configurando e recuperando as propriedades de um trabalho.](setting-and-retrieving-the-properties-of-a-job.md)

Windows PowerShell fornece um mecanismo simples para gerenciar muitas tarefas bits. Esta seção contém os seguintes tópicos que mostram como usar Windows PowerShell cmdlets com BITS:

-   [Usar o Windows PowerShell para criar trabalhos de transferência do BITS](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [Usar os cmdlets do Windows PowerShell do WinRM para gerenciar trabalhos de transferência do BITS](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [Usando cmdlets de Windows PowerShell WMI para gerenciar o bits compact server](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> A partir do Windows 10, versão 1607, você também pode executar cmdlets do PowerShell e usar BITSAdmin ou outros aplicativos que usam as [interfaces](bits-interfaces.md) BITS de uma linha de comando remota do PowerShell conectada a outro computador (físico ou virtual). Essa funcionalidade não está disponível ao usar uma linha de comando do [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) para uma máquina virtual na mesma máquina física e não está disponível ao usar cmdlets winRM.
>
> Um trabalho bits criado de uma sessão remota do PowerShell será executado no contexto da conta de usuário dessa sessão e só fará progresso quando houver pelo menos uma sessão de logon local ativa ou sessão remota do PowerShell associada a essa conta de usuário. Para obter mais informações, consulte [Para gerenciar sessões remotas do PowerShell.](using-windows-powershell-to-create-bits-transfer-jobs.md)

 

Esta seção também contém os seguintes tópicos:

-   [Práticas recomendadas ao usar BITS](best-practices-when-using-bits.md)
-   [Enumerando trabalhos na fila de transferência](enumerating-jobs-in-the-transfer-queue.md)
-   [Enumerando arquivos em um trabalho](enumerating-files-in-a-job.md)
-   [Tratando erros](handling-errors.md)
-   [Recuperar a resposta de um trabalho de upload/resposta](retrieving-the-reply-from-an-upload-reply-job.md)

Para ver o código de exemplo que usa as interfaces BITS, consulte [Amostras e ferramentas do BITS.](bits-samples-and-tools.md)

 

 