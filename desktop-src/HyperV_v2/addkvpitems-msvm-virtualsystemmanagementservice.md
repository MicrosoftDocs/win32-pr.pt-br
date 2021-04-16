---
description: Adiciona pares de chave-valor a uma máquina virtual.
ms.assetid: D952EC3D-24EB-4A68-8527-5BF522957CB6
title: Método AddKvpItems da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9e01a02615b8bb395a589160a765dec4e08526e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758809"
---
# <a name="addkvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="e7bbd-103">Método AddKvpItems da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="e7bbd-103">AddKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="e7bbd-104">Adiciona pares de chave-valor a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7bbd-104">Adds key-value pairs to a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7bbd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7bbd-105">Syntax</span></span>


```mof
uint32 AddKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e7bbd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7bbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7bbd-107">*TargetSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbd-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbd-108">Tipo: **[ **\_ sistema de ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="e7bbd-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="e7bbd-109">Uma referência a um objeto de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual na qual os pares de chave-valor serão adicionados.</span><span class="sxs-lookup"><span data-stu-id="e7bbd-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object that represents the virtual machine on which the key-value pairs will be added.</span></span>

</dd> <dt>

<span data-ttu-id="e7bbd-110">*DataItems* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbd-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbd-111">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e7bbd-111">Type: **string\[\]**</span></span>

<span data-ttu-id="e7bbd-112">Uma matriz de pares chave-valor a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="e7bbd-112">An array of key-value pairs to be added.</span></span> <span data-ttu-id="e7bbd-113">Cada elemento da matriz é uma instância incorporada da classe [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="e7bbd-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="e7bbd-114">Esse método falhará se qualquer um dos pares chave-valor especificados já existir no sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="e7bbd-114">This method fails if any of the specified key-value pairs already exists on the target system.</span></span> <span data-ttu-id="e7bbd-115">Essa matriz pode conter no máximo 128 elementos.</span><span class="sxs-lookup"><span data-stu-id="e7bbd-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="e7bbd-116">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e7bbd-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbd-117">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="e7bbd-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="e7bbd-118">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e7bbd-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7bbd-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7bbd-119">Return value</span></span>

<span data-ttu-id="e7bbd-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7bbd-120">Type: **uint32**</span></span>

<span data-ttu-id="e7bbd-121">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7bbd-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e7bbd-122">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-124">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-125">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-126">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-127">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-128">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-129">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-130">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-131">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-132">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-133">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e7bbd-134">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e7bbd-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e7bbd-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7bbd-135">Remarks</span></span>

<span data-ttu-id="e7bbd-136">O acesso à classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="e7bbd-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e7bbd-137">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e7bbd-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="e7bbd-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e7bbd-138">Examples</span></span>

<span data-ttu-id="e7bbd-139">O exemplo de C# a seguir adiciona pares de chave-valor a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7bbd-139">The following C# sample adds key-value pairs to a virtual machine.</span></span> <span data-ttu-id="e7bbd-140">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="e7bbd-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7bbd-141">Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="e7bbd-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public static void AddKvpItems(string vmName, string itemName, string itemValue)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("AddKvpItems");
    ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

    ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();

    dataItem["Data"] = itemValue;
    dataItem["Name"] = itemName;
    dataItem["Source"] = 0;

    string[] dataItems = new string[1];
    dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    inParams["TargetSystem"] = vm.Path.Path;
    inParams["DataItems"] = dataItems;

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("AddKvpItems", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Resources were added successfully.");

        }
        else
        {
            Console.WriteLine("Failed to add resources");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Resources were added successfully.");
    }
    else
    {
        Console.WriteLine("Add virtual system Kvp items failed with error {0}", outParams["ReturnValue"]);
    }

    if (inParams != null)
    {
        inParams.Dispose();
    }

    if (outParams != null)
    {
        outParams.Dispose();
    }
}
```



<span data-ttu-id="e7bbd-142">O exemplo de Visual Basic Scripting Edition (VBScript) a seguir adiciona pares de chave-valor a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7bbd-142">The following Visual Basic Scripting Edition (VBScript) sample adds key-value pairs to a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7bbd-143">Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="e7bbd-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, vmName, itemName, itemValue, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
        itemValue = objArgs.Unnamed.Item(2)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName itemValue"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if AddKvpItems(myVm, itemName, itemValue) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "AddKvpItems failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    dim query
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' AddKvpItems
'-----------------------------------------------------------------
Function AddKvpItems(computerSystem, itemName, itemValue)

    dim dataItem, dataItems, objInParam, objOutParams
    
    AddKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    dataItem.Data = itemValue
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("AddKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.DataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("AddKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            AddKvpItems = true
        end if
    elseif (objOutParams.ReturnValue = wmiSuccessful) then
        AddKvpItems = true
    else
        WriteLog Format1("AddKvpItem failed with error {0}", objOutParams.ReturnValue)
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    
    dim WMIJob, jobState
    WMIJobCompleted = true

    set WMIJob = objWMIService.Get(outParam.Job)
    
    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (WMIJob.JobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WMIJobCompleted = false
    end if
    
End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\AddKvpItems.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="e7bbd-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7bbd-144">Requirements</span></span>



| <span data-ttu-id="e7bbd-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7bbd-145">Requirement</span></span> | <span data-ttu-id="e7bbd-146">Valor</span><span class="sxs-lookup"><span data-stu-id="e7bbd-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7bbd-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7bbd-147">Minimum supported client</span></span><br/> | <span data-ttu-id="e7bbd-148">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e7bbd-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e7bbd-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7bbd-149">Minimum supported server</span></span><br/> | <span data-ttu-id="e7bbd-150">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e7bbd-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7bbd-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7bbd-151">Namespace</span></span><br/>                | <span data-ttu-id="e7bbd-152">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e7bbd-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e7bbd-153">MOF</span><span class="sxs-lookup"><span data-stu-id="e7bbd-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7bbd-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7bbd-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7bbd-155">DLL</span><span class="sxs-lookup"><span data-stu-id="e7bbd-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7bbd-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7bbd-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7bbd-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7bbd-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7bbd-158">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="e7bbd-158">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

