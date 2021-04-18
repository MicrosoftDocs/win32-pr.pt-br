---
description: Recupera a imagem em miniatura de uma máquina virtual existente.
ms.assetid: 8D670D2E-EAD7-47FF-B13C-764EFFDF4547
title: Método GetVirtualSystemThumbnailImage da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetVirtualSystemThumbnailImage
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2c8288d2acee5816c4546b968a9a26c083cbbc88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756763"
---
# <a name="getvirtualsystemthumbnailimage-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GetVirtualSystemThumbnailImage da \_ classe VirtualSystemManagementService Msvm

Recupera a imagem em miniatura de uma máquina virtual existente.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetVirtualSystemThumbnailImage(
  [in]  CIM_VirtualSystemSettingData REF TargetSystem,
  [in]  uint16                           WidthPixels,
  [in]  uint16                           HeightPixels,
  [out] uint8                            ImageData[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TargetSystem* \[ no\]
</dt> <dd>

Tipo: **CIM \_ VirtualSystemSettingData**

Uma referência à instância [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) cuja imagem em miniatura deve ser recuperada. Essa instância pode representar a instanciação atual da máquina virtual ou uma instância de um instantâneo da máquina virtual.

</dd> <dt>

*WidthPixels* \[ no\]
</dt> <dd>

Tipo: **UInt16**

A largura da imagem desejada, em pixels.

</dd> <dt>

*HeightPixels* \[ no\]
</dt> <dd>

Tipo: **UInt16**

A altura da imagem desejada, em pixels.

</dd> <dt>

*ImageData* \[ fora\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Os dados de imagem solicitados, em formato RGB bruto 565.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

O **status é desconhecido** (32771)
</dt> <dt>

**Tempo limite** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

O **sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

O **sistema não está disponível** (32777)
</dt> <dt>

**Memória insuficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemplos

O exemplo de C# a seguir recupera a imagem em miniatura de uma máquina virtual. Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.

 


```CSharp
static void SaveImageData(byte[] imageData)
{
    FileStream fs = new FileStream(@"c:\test.bin", FileMode.Create, FileAccess.Write);
    fs.Write(imageData, 0, imageData.Length);
    fs.Flush();
    fs.Close();
}

public static void GetVirtualSystemThumbnailImage(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");

    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);

    ManagementObjectCollection vmsettingDatas = vm.GetRelated(
        "Msvm_VirtualSystemsettingData",
        "Msvm_SettingsDefineState",
        null,
        null,
        "SettingData",
        "ManagedElement",
        false,
        null);

    ManagementObject settingData = null;

    foreach (ManagementObject data in vmsettingDatas)
    {
        settingData = data;
        break;
    }


    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetVirtualSystemThumbnailImage");
    inParams["HeightPixels"] = 16;
    inParams["WidthPixels"] = 16;
    inParams["TargetSystem"] = settingData.Path.Path;


    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetVirtualSystemThumbnailImage", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            SaveImageData((byte[])outParams["ImageData"]);
            Console.WriteLine("VM '{0}' thumbnail were retrieved successfully.", vm["ElementName"]);
        }
        else
        {
            Console.WriteLine("Failed to retrieve VM thumbnail");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        SaveImageData((byte[])outParams["ImageData"]);
        Console.WriteLine("VM '{0}' thumbnail were retrieved successfully.", vm["ElementName"]);
    }
    else
    {
        Console.WriteLine("Failed to retrieve VM thumbnail with error {0}", (UInt32)outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    settingData.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



O exemplo a seguir Visual Basic Scripting Edition (VBScript) recupera a imagem em miniatura de uma máquina virtual.

> [!IMPORTANT]
> Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.

 


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem

const wmiStarted = 4096
const wmiSuccessful = 0

Main()


'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, objArgs, vmName, vm
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")
    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)
    
    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 1 then
        vmName = objArgs.Unnamed.Item(0)
    else
        WScript.Echo "usage: cscript GetVirtualSystemThumbnailImage.vbs vmName"
        WScript.Quit(1)
    end if
    
    set vm = GetComputerSystem(vmName)
    
    if StartVm(vm) then
        if GetVirtualSystemThumbnailImage(vm) then
            WriteLog "Done"
            WScript.Quit(0)
         End if
    end if
    
    WriteLog "GetVirtualSystemThumbnailImage Failed."
    WScript.Quit(1)
    
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
' Save the thumbnail
'-----------------------------------------------------------------
Sub SaveThumbnailImage(thumbnailBytes)

    dim stream 
    Const adTypeText = 2
    Const adSaveCreateOverWrite = 2  
    
    set stream = CreateObject("ADODB.Stream")
    stream.Type = adTypeText
  
    stream.Open
    Redim text(ubound(thumbnailBytes) \ 2)
    for i = lbound(thumbnailBytes) to ubound(thumbnailBytes) step 2
        text(i\2) = ChrW(thumbnailBytes(i + 1) * &HFF + thumbnailBytes(i))
    next
    stream.WriteText text
  
    stream.SaveToFile ".\thumbnail.bin", adSaveCreateOverWrite
    stream.Close
    
  
End Sub

'-----------------------------------------------------------------
' Start the virtual machine 
'-----------------------------------------------------------------
Function StartVm(computerSystem)
    
    dim objInParam, objOutParams
    StartVm = false
    if computerSystem.OperationalStatus(0) = 2 then
        StartVm = true
        Exit Function
    end if
    
    set objInParam = computerSystem.Methods_("RequestStateChange").InParameters.SpawnInstance_()
    objInParam.RequestedState = 2
    set objOutParams = computerSystem.ExecMethod_("RequestStateChange", objInParam)
    
    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            StartVm = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        StartVm = true
    else
        WriteLog Format1("StartVM failed with ReturnValue {0}", wmiStatus)
    end if
    
End Function


'-----------------------------------------------------------------
' Print the thumbnail data
'-----------------------------------------------------------------
Sub PrintThumbnailImage(thumbnailBytes)
    dim index
    for index = lbound(thumbnailBytes) to ubound(thumbnailBytes)
        WriteLog Format2("{0}:{1} ", index, thumbnailBytes(i))
    next
End Sub
'-----------------------------------------------------------------
' Define a virtual system
'-----------------------------------------------------------------
Function GetVirtualSystemThumbnailImage(computerSystem)
    dim query, objInParam, objOutParams, virtualSystemsetting
    
    GetVirtualSystemThumbnailImage = false
    
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_VirtualSystemsettingData", computerSystem.Path_.Path)
    set virtualSystemsetting = objWMIService.ExecQuery(query).ItemIndex(0)
    
    set objInParam = managementService.Methods_("GetVirtualSystemThumbnailImage").InParameters.SpawnInstance_()

    objInParam.HeightPixels = 16
    objInParam.WidthPixels = 16
    objInParam.TargetSystem = virtualSystemsetting.Path_.Path
    
    set objOutParams = managementService.ExecMethod_("GetVirtualSystemThumbnailImage", objInParam)
    
    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            GetVirtualSystemThumbnailImage = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        GetVirtualSystemThumbnailImage = true
    else
        WriteLog Format1("GetVirtualSystemThumbnailImage failed with ReturnValue {0}", wmiStatus)
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    
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
    set fileStream = fileSystem.OpenTextFile(".\GetVirtualSystemThumbnailImage.log", 8, true)
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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

