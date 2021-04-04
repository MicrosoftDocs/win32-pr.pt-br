---
title: Managed Reference for BITS PowerShell Commands (Referência gerenciada para comandos do PowerShell do BITS)
description: Serviço de Transferência Inteligente em Segundo Plano (BITS) 4,0 podem usar cmdlets do Windows PowerShell para gerenciar trabalhos de transferência.
ms.assetid: 2c151dfe-4f89-41ea-a533-21ffcf0aa39e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bd195d2202849c2bf2df580d159ee401911c51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823882"
---
# <a name="managed-reference-for-bits-powershell-commands"></a>Managed Reference for BITS PowerShell Commands (Referência gerenciada para comandos do PowerShell do BITS)

Serviço de Transferência Inteligente em Segundo Plano (BITS) 4,0 podem usar os cmdlets do Windows PowerShell para criar e gerenciar o download de arquivos e carregar trabalhos de transferência.

```PowerShell
Import-Module BitsTransfer
mkdir -force c:\temp\BITSFILES
Start-BitsTransfer -Source https://aka.ms/WinServ16/StndPDF -Destination c:\temp\BITSFILES\WindowsServer2016.pdf
```

Os cmdlets do Windows PowerShell para BITS fornecem grande parte da mesma funcionalidade que o utilitário de linha de comando Bitsadmin. No entanto, o Windows PowerShell também faz o seguinte:

-   Automatiza tarefas de BITS em uma linguagem de script extensível e orientada por gerenciamento.
-   Fornece uma única ferramenta para todas as tarefas relacionadas ao trabalho.

> [!Note]  
> Para usar esses comandos, primeiro você deve importar o módulo do PowerShell do BITS, usando o `Import-Module BitsTransfer` comando. Para obter mais informações, consulte o seguinte [artigo do TechNet](/previous-versions/technet-magazine/ff382721(v=msdn.10)).

 

Para obter mais informações sobre como usar o Windows PowerShell, consulte [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).

## <a name="bits-powershell-classes"></a>Classes do PowerShell do BITS

**Namespace**: Microsoft. BackgroundIntelligentTransfer. Management

**Assembly**: System. Management. Automation

Essas classes de comando do BITS são implementadas pelo Windows PowerShell. Essas classes são incluídas neste Software Development Kit (SDK) apenas para fins de integridade. Os membros dessas classes não podem ser usados diretamente, nem devem ser usados para derivar outras classes.



| Classe                           | Descrição                                                                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AddBitsFileCommand**          | Adiciona um ou mais arquivos a um trabalho de transferência de BITS existente.<br/> Consulte o cmdlet [Add-bitfile](/previous-versions//dd347701(v=technet.10)) para obter informações detalhadas sobre os parâmetros e exemplos.<br/>                       |
| **ClearBitsTransferCommand**    | Cancela um trabalho de transferência de BITS.<br/> Consulte o cmdlet [Clear-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) para obter informações detalhadas sobre os parâmetros e exemplos.<br/>                                          |
| **CompleteBitsTransferCommand** | Conclui um trabalho de transferência de BITS.<br/> Consulte o cmdlet [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) para obter informações detalhadas sobre os parâmetros e exemplos.<br/>                                     |
| **GetBitsTransferCommand**      | Recupera o objeto BitsJob associado para um trabalho de transferência de BITS existente.<br/> Consulte o cmdlet [Get-BitsTransfer](/previous-versions//dd347701(v=technet.10)) para obter informações detalhadas sobre os parâmetros e exemplos.<br/> |
| **NewBitsTransferCommand**      | Cria um novo trabalho de transferência de BITS.<br/> Consulte o cmdlet [New-BitsTransfer](/previous-versions//dd347701(v=technet.10)) para obter informações detalhadas sobre os parâmetros e exemplos.<br/>                                           |
| **ResumeBitsTransferCommand**   | Retoma um trabalho de transferência de BITS.<br/> Consulte o cmdlet [resume-BitsTransfer](/previous-versions//dd347701(v=technet.10)) para obter informações detalhadas sobre os parâmetros e exemplos.<br/>                                            |
| **SetBitsTransferCommand**      | Modifica as propriedades de um trabalho de transferência de BITS existente.<br/> Consulte o cmdlet [set-BitsTransfer](/previous-versions//dd347701(v=technet.10)) para obter informações detalhadas sobre os parâmetros e exemplos.<br/>                  |
| **SuspendBitsTransferCommand**  | Suspende um trabalho de transferência de BITS.<br/> Consulte o cmdlet [Suspend-BitsTransfer](/previous-versions//dd347701(v=technet.10)) para obter informações detalhadas sobre os parâmetros e exemplos.<br/>                                          |



 

 

