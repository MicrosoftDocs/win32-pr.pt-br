---
title: Usando BITS
description: Usando BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- BITS
- Serviço de Transferência Inteligente em Segundo Plano, tarefas
- BITS de transferência de arquivo
- Usando BITS bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105753001"
---
# <a name="using-bits"></a>Usando BITS

As etapas a seguir mostram como executar uma transferência de arquivo usando as  [interfaces](bits-interfaces.md)do serviço de transferência inteligente em segundo plano (bits).

**Para executar uma transferência de arquivo**

1.  [Conectar-se ao serviço BITS](connecting-to-the-bits-service.md)
2.  [Criar um trabalho de transferência](creating-a-job.md)
3.  [Adicionar arquivos ao trabalho](adding-files-to-a-job.md)
4.  [Iniciar o trabalho](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [Determinar se o BITS transferiu com êxito os arquivos](determining-the-status-of-a-job.md)
6.  [Concluir o trabalho](completing-and-canceling-a-job.md)

As etapas anteriores mostram como transferir arquivos usando os valores de propriedade padrão para um trabalho. Você pode alterar o comportamento padrão alterando um ou mais dos valores de Propriedade do trabalho. Por exemplo, você pode alterar a prioridade em que o trabalho é processado em relação a outros trabalhos na fila, especificar sua própria configuração de proxy e registrar para receber a notificação de eventos quando o BITS transferiu os arquivos. Para obter mais informações, consulte [Configurando e recuperando as propriedades de um trabalho](setting-and-retrieving-the-properties-of-a-job.md).

O Windows PowerShell fornece um mecanismo simples para gerenciar muitas tarefas de BITS. Esta seção contém os seguintes tópicos que mostram como usar os cmdlets do Windows PowerShell com BITS:

-   [Usar o Windows PowerShell para criar trabalhos de transferência do BITS](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [Usar os cmdlets do Windows PowerShell do WinRM para gerenciar trabalhos de transferência do BITS](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [Usando os cmdlets WMI do Windows PowerShell para gerenciar o BITS Compact Server](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> A partir do Windows 10, versão 1607, você também pode executar cmdlets do PowerShell e usar o BITSAdmin ou outros aplicativos que usam as [interfaces](bits-interfaces.md) bits de uma linha de comando remota do PowerShell conectada a outro computador (físico ou virtual). Esse recurso não está disponível ao usar uma linha de comando [direto do PowerShell](/virtualization/hyper-v-on-windows/user_guide/vmsession) para uma máquina virtual no mesmo computador físico e não está disponível ao usar os cmdlets do WinRM.
>
> Um trabalho do BITS criado a partir de uma sessão remota do PowerShell será executado sob o contexto da conta de usuário da sessão e só fará o progresso quando houver pelo menos uma sessão de logon local ativa ou uma sessão remota do PowerShell associada a essa conta de usuário. Para obter mais informações, consulte [para gerenciar sessões remotas do PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md).

 

Esta seção também contém os seguintes tópicos:

-   [Práticas recomendadas ao usar o BITS](best-practices-when-using-bits.md)
-   [Enumerando trabalhos na fila de transferência](enumerating-jobs-in-the-transfer-queue.md)
-   [Enumerando arquivos em um trabalho](enumerating-files-in-a-job.md)
-   [Tratando erros](handling-errors.md)
-   [Recuperar a resposta de um trabalho de resposta de upload](retrieving-the-reply-from-an-upload-reply-job.md)

Para obter o código de exemplo que usa as interfaces BITS, consulte [exemplos e ferramentas do bits](bits-samples-and-tools.md).

 

 