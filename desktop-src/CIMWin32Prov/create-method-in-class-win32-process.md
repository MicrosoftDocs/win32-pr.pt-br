---
description: Criar&\# 8194; O método de classe WMI cria um novo processo.
ms.assetid: be80abec-fab4-4403-bc29-d0d4a38e3c87
ms.tgt_platform: multiple
title: Método Create da classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42c675f61fc8b42790aeb811ec275554b355a392
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769049"
---
# <a name="create-method-of-the-win32_process-class"></a>Método Create da \_ classe Process do Win32

O método **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cria um novo processo.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Linha de comando* \[ no\]
</dt> <dd>

Linha de comando a ser executada. O sistema adiciona um caractere nulo à linha de comando, cortando a cadeia de caracteres, se necessário, para indicar qual arquivo foi realmente usado.

</dd> <dt>

*CurrentDirectory* \[ no\]
</dt> <dd>

Unidade e diretório atuais para o processo filho. A cadeia de caracteres requer que o diretório atual seja resolvido para um caminho conhecido. Um usuário pode especificar um caminho absoluto ou um caminho relativo ao diretório de trabalho atual. Se esse parâmetro for **nulo**, o novo processo terá o mesmo caminho que o processo de chamada. Essa opção é fornecida principalmente para shells que devem iniciar um aplicativo e especificar a unidade inicial e o diretório de trabalho do aplicativo.

</dd> <dt>

*ProcessStartupInformation* \[ no\]
</dt> <dd>

A configuração de inicialização de um processo do Windows. Para obter mais informações, consulte [**Win32 \_ ProcessStartup**](win32-processstartup.md).

</dd> <dt>

*ProcessId* \[ fora\]
</dt> <dd>

Identificador de processo global que pode ser usado para identificar um processo. O valor é válido a partir do momento em que o processo é criado até o momento em que o processo é encerrado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) se o processo foi criado com êxito e qualquer outro número para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Conclusão bem-sucedida** (0)
</dt> <dt>

**Acesso negado** (2)
</dt> <dt>

**Privilégio insuficiente** (3)
</dt> <dt>

**Falha desconhecida** (8)
</dt> <dt>

**Caminho não encontrado** (9)
</dt> <dt>

**Parâmetro inválido** (21)
</dt> <dt>

**Outro** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

Você pode criar uma instância da classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) para configurar o processo antes de chamar esse método.

Um caminho totalmente qualificado deve ser especificado nos casos em que o programa a ser iniciado não está no caminho de pesquisa de Winmgmt.exe. Se o processo recém-criado tentar interagir com objetos no sistema de destino sem os privilégios de acesso apropriados, ele será encerrado sem notificação para esse método.

Por motivos de segurança, o método **Win32 \_ processo. Create** não pode ser usado para iniciar um processo interativo remotamente.

Os processos criados com o método de **processo do Win32 \_ . Create** são limitados pelo objeto de trabalho, a menos que o sinalizador **criar \_ BREAKAWAY \_ do \_ trabalho** seja especificado. Para obter mais informações, consulte [**Win32 \_ ProcessStartup**](win32-processstartup.md) e [**\_ \_ ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir demonstra como invocar um método CIM como se fosse um método de automação de SWbemObject.


```VB
on error resume next

set process = GetObject("winmgmts:Win32_Process")

result = process.Create ("notepad.exe",null,null,processid)

WScript.Echo "Method returned result = " & result
WScript.Echo "Id of new process is " & processid

if err <>0 then
 WScript.Echo Err.Description, "0x" & Hex(Err.Number)
end if
```



O exemplo do Perl a seguir demonstra como invocar um método CIM como se fosse um método de automação de SWbemObject.


```VB
use strict;
use Win32::OLE;

my ($process, $outParam, $processid, $inParam, $objMethod);

eval { $process = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_Process"); };

if (!$@ && defined $process)
{
 $objMethod = $process->Methods_("Create");

 #Spawn an instance of inParameters and assign the values.
 $inParam = $objMethod->inParameters->SpawnInstance_ if (defined $objMethod);
 $inParam->{CommandLine} = "notepad.exe";
 $inParam->{CurrentDirectory} = undef;
 $inParam->{ProcessStartupInformation} = undef;

 $outParam = $process->ExecMethod_("Create", $inParam) if (defined $inParam);
 if ($outParam->{ReturnValue})
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
 else
 {
  print "Method returned result = $outParam->{ReturnValue}\n";
  print "Id of new process is $outParam->{ProcessId}\n"
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



O exemplo de código VBScript a seguir cria um processo do bloco de notas no computador local. [**Win32 \_ ProcessStartup**](win32-processstartup.md) é usado para definir as configurações do processo.


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Process ID: " & intProcessID
End If
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

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> <dt>

[Tarefas do WMI: processos](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

