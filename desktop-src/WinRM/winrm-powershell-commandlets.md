---
title: Referência gerenciada para classes de comando WinRM do Windows PowerShell
description: Gerenciamento Remoto do Windows 2,0 (WinRM) pode usar os cmdlets do Windows PowerShell para gerenciamento do sistema. Os cmdlets do Windows PowerShell permitem que um administrador configure o WinRM e obtenha dados ou gerencie recursos.
ms.assetid: 1ecdd41e-7257-483a-9a20-ae817f5f5ebe
ms.tgt_platform: multiple
keywords:
- ConnectWSManCommand
- DisableWSManCredSSPCommand
- DisconnectWSManCommand
- EnableWSManCredSSPCommand
- GetWSManCredSSPCommand
- GetWSManInstanceCommand
- InvokeWSManActionCommand
- NewWSManInstanceCommand
- NewWSManSessionOptionCommand
- RemoveWSManInstanceCommand
- SetWSManInstanceCommand
- SetWSManQuickConfigCommand
- TestWSManCommand
- SessionOption
- Mecanismo deAutenticação
- ProxyAccessType
- ProxyAuthentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd74af81c1cec7874ec0e881dbc236f5dd94d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163916"
---
# <a name="managed-reference-for-winrm-windows-powershell-command-classes"></a>Referência gerenciada para classes de comando WinRM do Windows PowerShell

Gerenciamento Remoto do Windows 2,0 (WinRM) pode usar os cmdlets do Windows PowerShell para gerenciamento do sistema. Os cmdlets do Windows PowerShell permitem que um administrador configure o WinRM e obtenha dados ou gerencie recursos.

Os cmdlets do Windows PowerShell para WinRM fornecem a mesma funcionalidade que o utilitário de linha de comando do WinRM. No entanto, o Windows PowerShell também faz o seguinte:

-   Automatiza tarefas do WinRM em uma linguagem de script extensível e orientada por gerenciamento.
-   Fornece uma única ferramenta para todas as tarefas de gerenciamento.

Consulte [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) para obter mais informações.

## <a name="ws-management-windows-powershell-classes"></a>WS-Management classes do Windows PowerShell

**Namespace**: Microsoft. WsMan. Management

**Assembly**: System. Management. Automation

As classes de comando WinRM a seguir são implementadas pelo Windows PowerShell. Essas classes são incluídas neste Software Development Kit (SDK) apenas para fins de integridade. Os membros dessas classes não podem ser usados diretamente nem devem ser usados para derivar outras classes.



| Classe                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConnectWSManCommand          | Conecta-se ao serviço WinRM em um computador remoto. <br/> Consulte o cmdlet [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/>                                                                                                                                                                                                                                                                                                                                              |
| DisableWSManCredSSPCommand   | Desabilita a autenticação CredSSP em um cliente.<br/> Consulte o cmdlet [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) para obter informações detalhadas sobre os parâmetros e exemplos.<br/>                                                                                                                                                                                                                                                                                                                                           |
| DisconnectWSManCommand       | Desconecta-se do serviço WinRM em um computador remoto. <br/> Consulte o cmdlet [Disconnect-WSMan](/powershell/module/Microsoft.WsMan.Management/Disconnect-WSMan?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/>                                                                                                                                                                                                                                                                                                                                      |
| EnableWSManCredSSPCommand    | Habilita a autenticação CredSSP no cliente.<br/> Consulte o cmdlet [Enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/>                                                                                                                                                                                                                                                                                                                                               |
| GetWSManCredSSPCommand       | Obtém a configuração relacionada a CredSSP para o cliente.<br/> Consulte o cmdlet [Get-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/>                                                                                                                                                                                                                                                                                                                                         |
| GetWSManInstanceCommand      | Exibe informações de gerenciamento para uma instância do recurso especificada por um URI de recurso.<br/> Consulte o cmdlet [Get-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/>                                                                                                                                                                                                                                                                                                          |
| InvokeWSManActionCommand     | Invoca uma ação no objeto de destino especificado pelo URI de recurso e pelos seletores. <br/> Consulte o cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/>                                                                                                                                                                                                                                                                                                         |
| NewWSManInstanceCommand      | Cria uma nova instância de um recurso de gerenciamento. <br/> Consulte o cmdlet [New-WSManInstance](/powershell/module/Microsoft.WsMan.Management/New-WSManInstance?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/>                                                                                                                                                                                                                                                                                                                                             |
| NewWSManSessionOptionCommand | Cria uma tabela de hash de opção de sessão do WinRM para usar como parâmetros de entrada para os seguintes cmdlets do WSMan: [Get-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true), [set-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true), [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)e [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true). <br/> Consulte o [New-WSManSessionOption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/> |
| RemoveWSManInstanceCommand   | Exclui uma instância do recurso de gerenciamento. <br/> Consulte o cmdlet [Remove-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Remove-WSManInstance?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| SetWSManInstanceCommand      | Modifica informações de gerenciamento relacionadas a um recurso. <br/> Consulte o cmdlet [set-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/>                                                                                                                                                                                                                                                                                                                                       |
| SetWSManQuickConfigCommand   | Configura o computador local para gerenciamento remoto. <br/> Consulte o cmdlet [Set-WSManQuickConfig](/powershell/module/Microsoft.WsMan.Management/Set-WSManQuickConfig?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/>                                                                                                                                                                                                                                                                                                                                      |
| TestWSManCommand             | Testa se o serviço WinRM está em execução em um computador local ou remoto. <br/> Consulte o cmdlet [Test-WSMan]( /powershell/module/microsoft.wsman.management/test-wsman?view=powershell-7&preserve-view=true) para obter exemplos e informações detalhadas sobre os parâmetros.<br/>                                                                                                                                                                                                                                                                                                                        |
| SessionOption                | Define um conjunto de opções estendidas para a sessão do WS-Management.<br/> Consulte o cmdlet [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os valores possíveis.<br/>                                                                                                                                                                                                                                                                                                                             |



 

## <a name="ws-management-windows-powershell-enumerations"></a>WS-Management enumerações do Windows PowerShell

As enumerações a seguir são implementadas pelo Windows PowerShell. Essas enumerações são incluídas neste Software Development Kit (SDK) apenas para fins de integridade.



| Enumeração             | Descrição                                                                                                                                                                                                                                   |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mecanismo deAutenticação | Especifica o mecanismo de autenticação a ser usado no servidor. <br/> Consulte o cmdlet [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os valores possíveis.<br/>      |
| ProxyAccessType         | Especifica o mecanismo pelo qual o servidor proxy é localizado.<br/> Consulte o cmdlet [New-WSManSessionOption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os valores possíveis.<br/> |
| ProxyAuthentication     | Especifica o método de autenticação a ser usado no proxy.<br/> Consulte o cmdlet [New-WSManSessionOption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) para obter exemplos e informações detalhadas sobre os valores possíveis.<br/>      |



 

 

