---
description: Simula um pressionamento de tecla.
ms.assetid: 42C11F92-6143-40D7-9C07-56A6514EB4D1
title: Método PressKey da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.PressKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9f196c5af3f8946460564e56bb425ffc24b51c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756755"
---
# <a name="presskey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="f84eb-103">Método PressKey da classe de \_ teclado Msvm</span><span class="sxs-lookup"><span data-stu-id="f84eb-103">PressKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="f84eb-104">Simula um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="f84eb-104">Simulates a key press.</span></span> <span data-ttu-id="f84eb-105">Quando for bem-sucedida, a chave estará no estado inoperante.</span><span class="sxs-lookup"><span data-stu-id="f84eb-105">When successful the key will be in the down state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f84eb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f84eb-106">Syntax</span></span>


```mof
uint32 PressKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="f84eb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f84eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f84eb-108">*KeyCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f84eb-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f84eb-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f84eb-109">Type: **uint32**</span></span>

<span data-ttu-id="f84eb-110">O código de chave virtual da chave a ser pressionada.</span><span class="sxs-lookup"><span data-stu-id="f84eb-110">The virtual-key code of the key to press.</span></span> <span data-ttu-id="f84eb-111">Para obter a lista de códigos de chave virtual, consulte [**códigos de chave virtual**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f84eb-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f84eb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f84eb-112">Return value</span></span>

<span data-ttu-id="f84eb-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f84eb-113">Type: **uint32**</span></span>

<span data-ttu-id="f84eb-114">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="f84eb-114">A return value of zero indicates success.</span></span> <span data-ttu-id="f84eb-115">Um valor diferente de zero indica uma falha ao modificar o estado da chave.</span><span class="sxs-lookup"><span data-stu-id="f84eb-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="f84eb-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="f84eb-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f84eb-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="f84eb-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f84eb-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="f84eb-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f84eb-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="f84eb-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f84eb-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f84eb-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="f84eb-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f84eb-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="f84eb-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f84eb-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f84eb-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f84eb-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="f84eb-129">Remarks</span></span>

<span data-ttu-id="f84eb-130">O método **PressKey** mapeia referências ao **\_ menu VK** (18), **\_ controle VK** (17) e **VK \_ Shift** (16) para **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) e **VK \_ LSHIFT** (160), respectivamente, porque os códigos de **\_ menu VK**, **VK \_ Control** e **VK \_ Shift** Virtual Key não representam chaves reais em um teclado.</span><span class="sxs-lookup"><span data-stu-id="f84eb-130">The **PressKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="f84eb-131">O acesso à classe de [**\_ teclado Msvm**](msvm-keyboard.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="f84eb-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f84eb-132">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f84eb-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="f84eb-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f84eb-133">Examples</span></span>

<span data-ttu-id="f84eb-134">O exemplo de C# a seguir simula um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="f84eb-134">The following C# sample simulates a key press.</span></span> <span data-ttu-id="f84eb-135">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="f84eb-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class PressKeyClass
    {
        static ManagementObject GetComputerKeyboard(ManagementObject vm)
        {
            ManagementObjectCollection keyboardCollection = vm.GetRelated
            (
                "Msvm_Keyboard",
                "Msvm_SystemDevice",
                null,
                null,
                "PartComponent",
                "GroupComponent",
                false,
                null
            );

            ManagementObject keyboard = null;

            foreach (ManagementObject instance in keyboardCollection)
            {
                keyboard = instance;
                break;
            }

            return keyboard;
        }

        static void PressKey(string vmName, int keyCode)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("PressKey");

            inParams["keyCode"] = keyCode;

            ManagementBaseObject outParams = keyboard.InvokeMethod("PressKey", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Key {0} was pressed on {1}", keyCode, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to press key {0}' on {1}", keyCode, vm["ElementName"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            keyboard.Dispose();
            vm.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: PressKey vmName keyCode");
                return;
            }
            string vmName = args[0];
            int keyCode = int.Parse(args[1]);
            PressKey(args[0], keyCode);
        }

    }
}

```



<span data-ttu-id="f84eb-136">O exemplo a seguir Visual Basic Scripting Edition (VBScript) simula um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="f84eb-136">The following Visual Basic Scripting Edition (VBScript) sample simulates a key press.</span></span>


```VB
option explicit 

dim objWMIService
dim fileSystem
const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    
    dim computer, objArgs, vmName, computerSystem, keycode, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       keycode = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript PressKey.vbs vmName keycode"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if PressKey(keyboard, keycode) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "PressKey failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    dim query
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Retrieve Msvm_Keyboard from given computer system
' 
'-----------------------------------------------------------------
Function GetComputerKeyboard(computerSystem)
    dim query
    On Error Resume Next
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_Keyboard", computerSystem.Path_.Path)
    set GetComputerKeyboard = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function

'-----------------------------------------------------------------
' Press the key with the given key code on the given keyboard
'-----------------------------------------------------------------
Function PressKey(keyboard, keyCode)
    WriteLog Format2("PressKey({0}, {1})", keyboard.ElementName, keyCode)
    
    dim objInParam, objOutParams
    
    PressKey = false
    set objInParam = keyboard.Methods_("PressKey").InParameters.SpawnInstance_()
    objInParam.keyCode = keyCode

    set objOutParams = keyboard.ExecMethod_("PressKey", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("The key with code '{0}' is typed on {1}.", keyCode, keyboard.ElementName)
        PressKey = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\PressKey.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="f84eb-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f84eb-137">Requirements</span></span>



| <span data-ttu-id="f84eb-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f84eb-138">Requirement</span></span> | <span data-ttu-id="f84eb-139">Valor</span><span class="sxs-lookup"><span data-stu-id="f84eb-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f84eb-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f84eb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f84eb-141">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f84eb-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f84eb-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f84eb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f84eb-143">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f84eb-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f84eb-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="f84eb-144">Namespace</span></span><br/>                | <span data-ttu-id="f84eb-145">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f84eb-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f84eb-146">MOF</span><span class="sxs-lookup"><span data-stu-id="f84eb-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f84eb-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f84eb-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f84eb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f84eb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f84eb-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f84eb-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f84eb-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="f84eb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f84eb-151">**\_Teclado Msvm**</span><span class="sxs-lookup"><span data-stu-id="f84eb-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="f84eb-152">**Códigos de chave virtual**</span><span class="sxs-lookup"><span data-stu-id="f84eb-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

