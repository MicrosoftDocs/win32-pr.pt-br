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
# <a name="create-method-of-the-win32_process-class"></a><span data-ttu-id="9c1c6-103">Método Create da \_ classe Process do Win32</span><span class="sxs-lookup"><span data-stu-id="9c1c6-103">Create method of the Win32\_Process class</span></span>

<span data-ttu-id="9c1c6-104">O método **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cria um novo processo.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new process.</span></span>

<span data-ttu-id="9c1c6-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="9c1c6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9c1c6-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9c1c6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c1c6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c1c6-107">Syntax</span></span>


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a><span data-ttu-id="9c1c6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c1c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c1c6-109">*Linha de comando* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c1c6-109">*CommandLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1c6-110">Linha de comando a ser executada.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-110">Command line to execute.</span></span> <span data-ttu-id="9c1c6-111">O sistema adiciona um caractere nulo à linha de comando, cortando a cadeia de caracteres, se necessário, para indicar qual arquivo foi realmente usado.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-111">The system adds a null character to the command line, trimming the string if necessary, to indicate which file was actually used.</span></span>

</dd> <dt>

<span data-ttu-id="9c1c6-112">*CurrentDirectory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c1c6-112">*CurrentDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1c6-113">Unidade e diretório atuais para o processo filho.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-113">Current drive and directory for the child process.</span></span> <span data-ttu-id="9c1c6-114">A cadeia de caracteres requer que o diretório atual seja resolvido para um caminho conhecido.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-114">The string requires that the current directory resolves to a known path.</span></span> <span data-ttu-id="9c1c6-115">Um usuário pode especificar um caminho absoluto ou um caminho relativo ao diretório de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-115">A user can specify an absolute path or a path relative to the current working directory.</span></span> <span data-ttu-id="9c1c6-116">Se esse parâmetro for **nulo**, o novo processo terá o mesmo caminho que o processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-116">If this parameter is **NULL**, the new process will have the same path as the calling process.</span></span> <span data-ttu-id="9c1c6-117">Essa opção é fornecida principalmente para shells que devem iniciar um aplicativo e especificar a unidade inicial e o diretório de trabalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-117">This option is provided primarily for shells that must start an application and specify the application's initial drive and working directory.</span></span>

</dd> <dt>

<span data-ttu-id="9c1c6-118">*ProcessStartupInformation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c1c6-118">*ProcessStartupInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1c6-119">A configuração de inicialização de um processo do Windows.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-119">The startup configuration of a Windows process.</span></span> <span data-ttu-id="9c1c6-120">Para obter mais informações, consulte [**Win32 \_ ProcessStartup**](win32-processstartup.md).</span><span class="sxs-lookup"><span data-stu-id="9c1c6-120">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c1c6-121">*ProcessId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9c1c6-121">*ProcessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1c6-122">Identificador de processo global que pode ser usado para identificar um processo.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-122">Global process identifier that can be used to identify a process.</span></span> <span data-ttu-id="9c1c6-123">O valor é válido a partir do momento em que o processo é criado até o momento em que o processo é encerrado.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-123">The value is valid from the time the process is created until the time the process is terminated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c1c6-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c1c6-124">Return value</span></span>

<span data-ttu-id="9c1c6-125">Retorna um valor de 0 (zero) se o processo foi criado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-125">Returns a value of 0 (zero) if the process was successfully created, and any other number to indicate an error.</span></span> <span data-ttu-id="9c1c6-126">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9c1c6-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9c1c6-127">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9c1c6-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9c1c6-128">**Conclusão bem-sucedida** (0)</span><span class="sxs-lookup"><span data-stu-id="9c1c6-128">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c1c6-129">**Acesso negado** (2)</span><span class="sxs-lookup"><span data-stu-id="9c1c6-129">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9c1c6-130">**Privilégio insuficiente** (3)</span><span class="sxs-lookup"><span data-stu-id="9c1c6-130">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9c1c6-131">**Falha desconhecida** (8)</span><span class="sxs-lookup"><span data-stu-id="9c1c6-131">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9c1c6-132">**Caminho não encontrado** (9)</span><span class="sxs-lookup"><span data-stu-id="9c1c6-132">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9c1c6-133">**Parâmetro inválido** (21)</span><span class="sxs-lookup"><span data-stu-id="9c1c6-133">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="9c1c6-134">**Outro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="9c1c6-134">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="9c1c6-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c1c6-135">Remarks</span></span>

<span data-ttu-id="9c1c6-136">Você pode criar uma instância da classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) para configurar o processo antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-136">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process before calling this method.</span></span>

<span data-ttu-id="9c1c6-137">Um caminho totalmente qualificado deve ser especificado nos casos em que o programa a ser iniciado não está no caminho de pesquisa de Winmgmt.exe.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-137">A fully qualified path must be specified in cases where the program to be launched is not in the search path of Winmgmt.exe.</span></span> <span data-ttu-id="9c1c6-138">Se o processo recém-criado tentar interagir com objetos no sistema de destino sem os privilégios de acesso apropriados, ele será encerrado sem notificação para esse método.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-138">If the newly created process attempts to interact with objects on the target system without the appropriate access privileges, it is terminated without notification to this method.</span></span>

<span data-ttu-id="9c1c6-139">Por motivos de segurança, o método **Win32 \_ processo. Create** não pode ser usado para iniciar um processo interativo remotamente.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-139">For security reasons the **Win32\_Process.Create** method cannot be used to start an interactive process remotely.</span></span>

<span data-ttu-id="9c1c6-140">Os processos criados com o método de **processo do Win32 \_ . Create** são limitados pelo objeto de trabalho, a menos que o sinalizador **criar \_ BREAKAWAY \_ do \_ trabalho** seja especificado.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-140">Processes created with the **Win32\_Process.Create** method are limited by the job object unless the **CREATE\_BREAKAWAY\_FROM\_JOB** flag is specified.</span></span> <span data-ttu-id="9c1c6-141">Para obter mais informações, consulte [**Win32 \_ ProcessStartup**](win32-processstartup.md) e [**\_ \_ ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span><span class="sxs-lookup"><span data-stu-id="9c1c6-141">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md) and [**\_\_ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span></span>

## <a name="examples"></a><span data-ttu-id="9c1c6-142">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9c1c6-142">Examples</span></span>

<span data-ttu-id="9c1c6-143">O exemplo de VBScript a seguir demonstra como invocar um método CIM como se fosse um método de automação de SWbemObject.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-143">The following VBScript example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


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



<span data-ttu-id="9c1c6-144">O exemplo do Perl a seguir demonstra como invocar um método CIM como se fosse um método de automação de SWbemObject.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-144">The following Perl example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


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



<span data-ttu-id="9c1c6-145">O exemplo de código VBScript a seguir cria um processo do bloco de notas no computador local.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-145">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="9c1c6-146">[**Win32 \_ ProcessStartup**](win32-processstartup.md) é usado para definir as configurações do processo.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-146">[**Win32\_ProcessStartup**](win32-processstartup.md) is used to configure the process settings.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9c1c6-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c1c6-147">Requirements</span></span>



| <span data-ttu-id="9c1c6-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c1c6-148">Requirement</span></span> | <span data-ttu-id="9c1c6-149">Valor</span><span class="sxs-lookup"><span data-stu-id="9c1c6-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c1c6-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c1c6-150">Minimum supported client</span></span><br/> | <span data-ttu-id="9c1c6-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c1c6-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9c1c6-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c1c6-152">Minimum supported server</span></span><br/> | <span data-ttu-id="9c1c6-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c1c6-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9c1c6-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="9c1c6-154">Namespace</span></span><br/>                | <span data-ttu-id="9c1c6-155">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9c1c6-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9c1c6-156">MOF</span><span class="sxs-lookup"><span data-stu-id="9c1c6-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c1c6-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c1c6-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c1c6-158">DLL</span><span class="sxs-lookup"><span data-stu-id="9c1c6-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c1c6-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c1c6-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c1c6-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c1c6-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c1c6-161">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9c1c6-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9c1c6-162">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="9c1c6-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="9c1c6-163">Tarefas do WMI: processos</span><span class="sxs-lookup"><span data-stu-id="9c1c6-163">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

