---
description: O&de GetOwner \# 8194; O método de classe WMI recupera o nome de usuário e o nome de domínio sob os quais o processo está sendo executado.
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Método GetOwner da classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089099"
---
# <a name="getowner-method-of-the-win32_process-class"></a><span data-ttu-id="06e8d-103">Método GetOwner da classe de \_ processo do Win32</span><span class="sxs-lookup"><span data-stu-id="06e8d-103">GetOwner method of the Win32\_Process class</span></span>

<span data-ttu-id="06e8d-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwner** recupera o nome de usuário e o nome de domínio sob o qual o processo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="06e8d-104">The **GetOwner** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the user name and domain name under which the process is running.</span></span>

<span data-ttu-id="06e8d-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="06e8d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="06e8d-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="06e8d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="06e8d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06e8d-107">Syntax</span></span>


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="06e8d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06e8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e8d-109">*Usuário* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="06e8d-109">*User* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06e8d-110">Retorna o nome de usuário do proprietário deste processo.</span><span class="sxs-lookup"><span data-stu-id="06e8d-110">Returns the user name of the owner of this process.</span></span>

</dd> <dt>

<span data-ttu-id="06e8d-111">*Domínio* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="06e8d-111">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06e8d-112">Retorna o nome de domínio no qual esse processo está em execução.</span><span class="sxs-lookup"><span data-stu-id="06e8d-112">Returns the domain name under which this process is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e8d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06e8d-113">Return value</span></span>

<span data-ttu-id="06e8d-114">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="06e8d-114">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="06e8d-115">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="06e8d-115">Any other number indicates an error.</span></span> <span data-ttu-id="06e8d-116">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="06e8d-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="06e8d-117">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="06e8d-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="06e8d-118">**Conclusão bem-sucedida** (0)</span><span class="sxs-lookup"><span data-stu-id="06e8d-118">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06e8d-119">**Acesso negado** (2)</span><span class="sxs-lookup"><span data-stu-id="06e8d-119">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06e8d-120">**Privilégio insuficiente** (3)</span><span class="sxs-lookup"><span data-stu-id="06e8d-120">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06e8d-121">**Falha desconhecida** (8)</span><span class="sxs-lookup"><span data-stu-id="06e8d-121">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="06e8d-122">**Caminho não encontrado** (9)</span><span class="sxs-lookup"><span data-stu-id="06e8d-122">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="06e8d-123">**Parâmetro inválido** (21)</span><span class="sxs-lookup"><span data-stu-id="06e8d-123">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="06e8d-124">**Outro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="06e8d-124">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="06e8d-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="06e8d-125">Examples</span></span>

<span data-ttu-id="06e8d-126">[A porcentagem de CPU do processo de monitor por nome com o proprietário](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) O exemplo de VBScript coleta a porcentagem de utilização da CPU ou do processador e pesquisa o proprietário do processo.</span><span class="sxs-lookup"><span data-stu-id="06e8d-126">[The Monitor Process CPU Pct by Name with Owner](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) VBScript sample collects the CPU or Processor utilization percent and looks up the process owner.</span></span>

<span data-ttu-id="06e8d-127">O exemplo [obter todos os servidores que uma lista de usuários está conectado](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) ao PowerShell consulta o WMI para o proprietário de todos os processos de explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="06e8d-127">The [Get all servers that a list of users is logged onto](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) PowerShell sample querys WMI for the owner of all explorer.exe processes.</span></span>

<span data-ttu-id="06e8d-128">O exemplo de código VBScript a seguir obtém o proprietário de cada processo em execução.</span><span class="sxs-lookup"><span data-stu-id="06e8d-128">The following VBScript code example obtains the owner for each running process.</span></span>


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="06e8d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06e8d-129">Requirements</span></span>



| <span data-ttu-id="06e8d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="06e8d-130">Requirement</span></span> | <span data-ttu-id="06e8d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="06e8d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06e8d-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06e8d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="06e8d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06e8d-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06e8d-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06e8d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="06e8d-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06e8d-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06e8d-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="06e8d-136">Namespace</span></span><br/>                | <span data-ttu-id="06e8d-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="06e8d-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06e8d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="06e8d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06e8d-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06e8d-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06e8d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="06e8d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06e8d-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06e8d-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06e8d-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="06e8d-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="06e8d-143">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="06e8d-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="06e8d-144">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="06e8d-144">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

