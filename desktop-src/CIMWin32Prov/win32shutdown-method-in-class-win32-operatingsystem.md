---
description: Win32Shutdown &\# 8194; O método de classe WMI fornece o conjunto completo de opções de desligamento com suporte dos sistemas operacionais Win32. Isso inclui fazer logoff, desligamento, reinicialização e forçar um logoff, desligamento ou reinicialização.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Método Win32Shutdown da classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826615"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a>Método Win32Shutdown da classe de sistema \_ operacional Win32

O método de   [classe WMI](../wmisdk/retrieving-a-class.md) **Win32Shutdown** fornece o conjunto completo de opções de desligamento com suporte dos sistemas operacionais Win32. Isso inclui fazer logoff, desligamento, reinicialização e forçar um logoff, desligamento ou reinicialização.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](../wmisdk/calling-a-method.md).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Conjunto de sinalizadores de bitmap para desligar o computador. Para forçar um comando, adicione o sinalizador Force (4) ao valor do comando. O uso da força em conjunto com o desligamento ou reinicialização em um computador remoto desliga imediatamente tudo (incluindo WMI, COM e assim por diante) ou reinicia o computador remoto. Isso resulta em um valor de retorno indeterminado.

<dt>

0 (0x0)
</dt> <dd>

**Logoff – faz** logoff do usuário no computador. O logoff interrompe todos os processos associados ao contexto de segurança do processo que chamou a função Exit, registra o usuário atual fora do sistema e exibe a caixa de diálogo de logon.

</dd> <dt>

4 (0x4)
</dt> <dd>

Logoff **forçado (0 + 4)** – registra o usuário no computador imediatamente e não notifica os aplicativos que a sessão de logon está encerrando. Isso pode resultar em perda de dados.

</dd> <dt>

1 (0x1)
</dt> <dd>

**Desligar** – desliga o computador a um ponto em que é seguro desligar o poder. (Todos os buffers de arquivo são liberados para o disco e todos os processos em execução são interrompidos.) Os usuários veem a mensagem, `It is now safe to turn off your computer.`

Durante o desligamento, o sistema envia uma mensagem para cada aplicativo em execução. Os aplicativos executam qualquer limpeza durante o processamento da mensagem e retornam true para indicar que eles podem ser encerrados.

</dd> <dt>

5 (0x5)
</dt> <dd>

**Desligamento forçado (1 + 4)** – desliga o computador a um ponto em que é seguro desligar o poder. (Todos os buffers de arquivo são liberados para o disco e todos os processos em execução são interrompidos.) Os usuários veem a mensagem,` It is now safe to turn off your computer.`

Quando a abordagem de desligamento forçado é usada, todos os serviços, incluindo WMI, são desligados imediatamente. Por isso, não será possível receber um valor de retorno se você estiver executando o script em um computador remoto.

</dd> <dt>

2 (0x2)
</dt> <dd>

**Reinicializar** – desliga e reinicia o computador.

</dd> <dt>

6 (0x6)
</dt> <dd>

**Reinicialização forçada (2 + 4)** – desliga e reinicia o computador.

Quando a abordagem de reinicialização forçada é usada, todos os serviços, incluindo WMI, são desligados imediatamente. Por isso, não será possível receber um valor de retorno se você estiver executando o script em um computador remoto.

</dd> <dt>

8 (0x8)
</dt> <dd>

**Desligar – desliga** o computador e desliga a energia (se houver suporte do computador em questão).

</dd> <dt>

12 (0xC)
</dt> <dd>

Desligamento **forçado (8 + 4)** – desliga o computador e desliga a energia (se houver suporte para o computador em questão).

Quando a abordagem de desligamento forçado é usada, todos os serviços, incluindo WMI, são desligados imediatamente. Por isso, não será possível receber um valor de retorno se você estiver executando o script em um computador remoto.

</dd> </dl> </dd> <dt>

*Reservado* \[ para no\]
</dt> <dd>

Um meio para estender **Win32Shutdown**. Atualmente, o parâmetro *reservado* é ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero (0) para indicar êxito. Qualquer outro número indica um erro. Para códigos de erro, consulte [**constantes de erro WMI**](../wmisdk/wmi-error-constants.md) ou [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](../debug/system-error-codes.md).

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Outro** (1 a 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

Para um gerenciamento mais eficiente de computadores em uma organização, os administradores precisam da capacidade de desligar ou reiniciar remotamente um computador ou fazer logoff remoto de um usuário. A capacidade de realizar essas tarefas permite que os administradores instalem software, reconfigurem as configurações do computador, removam computadores da rede e executem outras tarefas sem precisar desligar ou reiniciar manualmente cada computador.

Por exemplo, para executar uma atualização de rede, talvez seja necessário desligar todos os computadores em execução em um segmento de rede específico. Para forçar uma atualização de Política de Grupo, você precisa registrar os usuários em seus computadores. Se um vírus de computador estiver presente em qualquer lugar da sua organização, talvez você queira desligar o máximo possível de computadores, antes que o vírus tenha a oportunidade de se espalhar. A capacidade de desligar e reiniciar computadores e fazer logoff de usuários programaticamente em vez de manualmente pode ser um enorme economia de tempo.

O processo de chamada deve ter o privilégio de **\_ \_ nome de desligamento se** .

O método [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) fornece o mesmo conjunto de opções de desligamento com suporte pelo método **Win32Shutdown** no sistema [**\_ operacional Win32**](win32-operatingsystem.md) , mas também permite que você especifique comentários, um motivo para o desligamento ou um tempo limite.

O método Win32Shutdown não tem um parâmetro para bloquear uma estação de trabalho, deixando o usuário conectado. No entanto, as estações de trabalho podem ser bloqueadas na linha de comando usando o seguinte comando:

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a>Exemplos

O exemplo do VBScript [fazer logoff, reinicializar ou desligar vários computadores](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) na galeria do TechNet usa Win32Shutdown para fazer logoff, desligar, reinicializar ou desligar (dependendo da seleção) os computadores listados na matriz de servidores.

O [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) exemplo do PowerShell na galeria do TechNet inclui um método que chama Win32Shutdown em um computador remoto.

O exemplo do PowerShell a seguir usa o método Win32Shutdown para desligar o computador especificado.


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



O exemplo de código do PowerShell a seguir usa o EnableAllPrivileges do cmdlet Get-WmiObject para atingir os privilégios apropriados.


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



O código de exemplo VB.NET a seguir usa o método Shutdown para reinicializar ou fazer logoff de um sistema.


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> <dt>

[**Sistema \_ operacional Win32**](win32-operatingsystem.md)
</dt> <dt>

[**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[Tarefas do WMI: gerenciamento de desktop](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[Executando operações privilegiadas usando o VBScript](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
