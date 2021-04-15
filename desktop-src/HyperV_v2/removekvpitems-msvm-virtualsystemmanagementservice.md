---
description: Remove os pares de chave-valor existentes de uma máquina virtual.
ms.assetid: B2ECF609-89BB-4117-982B-EF56D51E1321
title: Método RemoveKvpItems da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4921805ade9538a4e05a15331f707b9356411aa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506209"
---
# <a name="removekvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="47c88-103">Método RemoveKvpItems da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="47c88-103">RemoveKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="47c88-104">Remove os pares de chave-valor existentes de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="47c88-104">Removes existing key-value pairs from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c88-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47c88-105">Syntax</span></span>


```mof
uint32 RemoveKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="47c88-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47c88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47c88-107">*TargetSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47c88-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c88-108">Tipo: **[ **\_ sistema de ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="47c88-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="47c88-109">Uma referência à máquina virtual na qual os pares de chave-valor serão removidos.</span><span class="sxs-lookup"><span data-stu-id="47c88-109">A reference to the virtual machine on which the key-value pairs will be removed.</span></span>

</dd> <dt>

<span data-ttu-id="47c88-110">*DataItems* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47c88-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c88-111">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47c88-111">Type: **string\[\]**</span></span>

<span data-ttu-id="47c88-112">Uma matriz de pares chave-valor a ser removida (somente as chaves precisam corresponder).</span><span class="sxs-lookup"><span data-stu-id="47c88-112">An array of key-value pairs to be removed (only the keys need to match).</span></span> <span data-ttu-id="47c88-113">Cada elemento da matriz é uma instância incorporada da classe [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="47c88-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="47c88-114">Esse método falhará se qualquer um dos pares chave-valor especificados não existir no sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="47c88-114">This method fails if any of the specified key-value pairs does not exist on the target system.</span></span> <span data-ttu-id="47c88-115">Essa matriz pode conter no máximo 128 elementos.</span><span class="sxs-lookup"><span data-stu-id="47c88-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="47c88-116">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="47c88-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c88-117">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="47c88-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="47c88-118">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="47c88-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47c88-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47c88-119">Return value</span></span>

<span data-ttu-id="47c88-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47c88-120">Type: **uint32**</span></span>

<span data-ttu-id="47c88-121">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="47c88-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="47c88-122">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="47c88-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="47c88-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-124">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="47c88-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-125">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="47c88-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-126">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="47c88-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-127">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="47c88-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-128">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="47c88-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-129">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="47c88-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-130">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="47c88-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-131">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="47c88-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-132">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="47c88-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-133">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="47c88-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="47c88-134">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="47c88-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="47c88-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="47c88-135">Remarks</span></span>

<span data-ttu-id="47c88-136">O acesso à classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="47c88-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="47c88-137">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="47c88-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="47c88-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47c88-138">Examples</span></span>

<span data-ttu-id="47c88-139">O exemplo de C# a seguir remove os pares de chave-valor de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="47c88-139">The following C# sample removes key-value pairs from a virtual machine.</span></span> <span data-ttu-id="47c88-140">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="47c88-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47c88-141">Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="47c88-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public static void RemoveKvpItems(string vmName, string itemName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("RemoveKvpItems");
    ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

    ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();

    dataItem["Data"] = "";
    dataItem["Name"] = itemName;
    dataItem["Source"] = 0;

    string[] dataItems = new string[1];
    dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    inParams["TargetSystem"] = vm.Path.Path;
    inParams["DataItems"] = dataItems;

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("RemoveKvpItems", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("KvpItems were removed successfully.");

        }
        else
        {
            Console.WriteLine("Failed to remove KvpItems");
        }
    } 
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("KvpItems were removed successfully.");
    }
    else
    {
        Console.WriteLine("Remove KvpItems failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    dataItem.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
    
}
```



<span data-ttu-id="47c88-142">O exemplo de Visual Basic Scripting Edition (VBScript) a seguir remove os pares de chave-valor de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="47c88-142">The following Visual Basic Scripting Edition (VBScript) sample removes key-value pairs from a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47c88-143">Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="47c88-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


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

    dim computer, vmName, itemName, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if RemoveKvpItems(myVm, itemName) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "RemoveKvpItems failed"
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
' RemoveKvpItems
'-----------------------------------------------------------------
Function RemoveKvpItems(computerSystem, itemName)

    dim dataItem, dataItems, objInParam, objOutParams
    
    RemoveKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    dataItem.Data = ""
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("RemoveKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.dataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("RemoveKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            RemoveKvpItems = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        RemoveKvpItems = true
    else
        WriteLog Format1("RemoveKvpItems failed with {0}", objOutParams.ReturnValue )
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
    set fileStream = fileSystem.OpenTextFile(".\RemoveKvpItems.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="47c88-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47c88-144">Requirements</span></span>



| <span data-ttu-id="47c88-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="47c88-145">Requirement</span></span> | <span data-ttu-id="47c88-146">Valor</span><span class="sxs-lookup"><span data-stu-id="47c88-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c88-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47c88-147">Minimum supported client</span></span><br/> | <span data-ttu-id="47c88-148">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="47c88-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="47c88-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47c88-149">Minimum supported server</span></span><br/> | <span data-ttu-id="47c88-150">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="47c88-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47c88-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="47c88-151">Namespace</span></span><br/>                | <span data-ttu-id="47c88-152">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="47c88-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="47c88-153">MOF</span><span class="sxs-lookup"><span data-stu-id="47c88-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47c88-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47c88-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="47c88-155">DLL</span><span class="sxs-lookup"><span data-stu-id="47c88-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47c88-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47c88-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="47c88-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="47c88-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c88-158">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="47c88-158">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

