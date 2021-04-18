---
description: Cria um arquivo de disquete virtual.
ms.assetid: C7B5712C-55DD-4784-8B2E-A8DE02E4CFD8
title: Método CreateVirtualFloppyDisk da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualFloppyDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 98781a4f72218ee61a4966dc76b21f7417353e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753295"
---
# <a name="createvirtualfloppydisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="7eb32-103">Método CreateVirtualFloppyDisk da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="7eb32-103">CreateVirtualFloppyDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="7eb32-104">Cria um arquivo de disquete virtual.</span><span class="sxs-lookup"><span data-stu-id="7eb32-104">Creates a virtual floppy disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb32-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7eb32-105">Syntax</span></span>


```mof
uint32 CreateVirtualFloppyDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7eb32-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7eb32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eb32-107">*Caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7eb32-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb32-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7eb32-108">Type: **string**</span></span>

<span data-ttu-id="7eb32-109">Um caminho totalmente qualificado que especifica o local do novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="7eb32-109">A fully qualified path that specifies the location of the new file.</span></span>

</dd> <dt>

<span data-ttu-id="7eb32-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="7eb32-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb32-111">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="7eb32-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="7eb32-112">Uma referência ao trabalho (pode ser **NULL** se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="7eb32-112">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eb32-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7eb32-113">Return value</span></span>

<span data-ttu-id="7eb32-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7eb32-114">Type: **uint32**</span></span>

<span data-ttu-id="7eb32-115">Esse método pode retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7eb32-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7eb32-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="7eb32-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="7eb32-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="7eb32-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="7eb32-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="7eb32-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="7eb32-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="7eb32-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="7eb32-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="7eb32-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="7eb32-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="7eb32-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="7eb32-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="7eb32-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="7eb32-129">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="7eb32-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="7eb32-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="7eb32-130">Remarks</span></span>

<span data-ttu-id="7eb32-131">O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="7eb32-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7eb32-132">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7eb32-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="7eb32-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7eb32-133">Examples</span></span>

<span data-ttu-id="7eb32-134">O exemplo C# a seguir cria um arquivo de disquete virtual.</span><span class="sxs-lookup"><span data-stu-id="7eb32-134">The following C# example creates a virtual floppy disk file.</span></span> <span data-ttu-id="7eb32-135">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="7eb32-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class CreateVFD
    {
        static void CreateVirtualFlopy(string vhdPath)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

            ManagementBaseObject inParams = imageService.GetMethodParameters("CreateVirtualFloppyDisk");
            inParams["Path"] = vhdPath;
            ManagementBaseObject outParams = imageService.InvokeMethod("CreateVirtualFloppyDisk", inParams, null);
            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("{0} was created successfully.", inParams["Path"]);
                }
                else
                {
                    Console.WriteLine("Unable to create {0}", inParams["Path"]);
                }
            }

            inParams.Dispose();
            outParams.Dispose();
            imageService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 1)
            {
                Console.WriteLine("Usage: CreateVFD path");
                return;
            }
            CreateVirtualFlopy(args[0]);
        }
    }
}

```



<span data-ttu-id="7eb32-136">O exemplo a seguir Visual Basic Scripting Edition (VBScript) cria um arquivo de disquete virtual.</span><span class="sxs-lookup"><span data-stu-id="7eb32-136">The following Visual Basic Scripting Edition (VBScript) example creates a virtual floppy disk file.</span></span>


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096

const method = "CreateVirtualFloppyDisk"
Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, objArgs, vfdPath

    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("Select * from Msvm_ImageManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 1 then
       vfdPath = objArgs.Unnamed.Item(0)
    else
       WScript.Echo "usage: cscript CreateVFD.vbs VFDFilePath "
       WScript.Quit(1)
    end if

    if CreateVirtualFloppyDisk(vfdPath) then
        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "CreateVFD failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Execute CreateVirtualFloppyDisk method
'-----------------------------------------------------------------
Function CreateVirtualFloppyDisk(vfdPath)
    WriteLog Format1("Function CreateVirtualFloppyDisk({0})",  vfdPath)
    
    dim objInParam, objOutParams

    CreateVirtualFloppyDisk = false

    set objInParam = managementService.Methods_("CreateVirtualFloppyDisk").InParameters.SpawnInstance_()
    objInParam.Path = vfdPath

    set objOutParams = managementService.ExecMethod_("CreateVirtualFloppyDisk", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VHD {0} was created successfully", vfdPath)
            CreateVirtualFloppyDisk = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)
    WriteLog "Function WMIMethodStarted"
    
    dim wmiStatus
    
    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        else
            WriteLog Format2("Failed to create VFD {0} ConcreteJob with error {1}", vfdPath, wmiStatus)
        end if
   end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    WriteLog "Function WMIJobCompleted"
    dim WMIJob, jobState

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\CreateVFD.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="7eb32-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eb32-137">Requirements</span></span>



| <span data-ttu-id="7eb32-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eb32-138">Requirement</span></span> | <span data-ttu-id="7eb32-139">Valor</span><span class="sxs-lookup"><span data-stu-id="7eb32-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb32-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eb32-140">Minimum supported client</span></span><br/> | <span data-ttu-id="7eb32-141">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7eb32-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7eb32-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eb32-142">Minimum supported server</span></span><br/> | <span data-ttu-id="7eb32-143">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7eb32-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7eb32-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="7eb32-144">Namespace</span></span><br/>                | <span data-ttu-id="7eb32-145">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7eb32-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7eb32-146">MOF</span><span class="sxs-lookup"><span data-stu-id="7eb32-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7eb32-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7eb32-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7eb32-148">DLL</span><span class="sxs-lookup"><span data-stu-id="7eb32-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eb32-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7eb32-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7eb32-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="7eb32-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="7eb32-151">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7eb32-151">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7eb32-152">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="7eb32-152">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

