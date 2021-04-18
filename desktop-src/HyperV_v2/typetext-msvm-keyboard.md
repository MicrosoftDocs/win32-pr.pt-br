---
description: Simula uma série de caracteres digitados.
ms.assetid: 5D4C9F27-84AA-4131-A9A3-2C72DB2E8909
title: Método TypeText da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeText
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 37e8227a545975a6193be63a8bd363e10e9805f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811027"
---
# <a name="typetext-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="e70ca-103">Método TypeText da classe de \_ teclado Msvm</span><span class="sxs-lookup"><span data-stu-id="e70ca-103">TypeText method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="e70ca-104">Simula uma série de caracteres digitados.</span><span class="sxs-lookup"><span data-stu-id="e70ca-104">Simulates a series of typed characters.</span></span> <span data-ttu-id="e70ca-105">Isso é equivalente a chamar [**PressKey**](presskey-msvm-keyboard.md) seguido por [**ReleaseKey**](releasekey-msvm-keyboard.md) para cada caractere na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e70ca-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md) for each character in the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70ca-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e70ca-106">Syntax</span></span>


```mof
uint32 TypeText(
  [in] string asciiText
);
```



## <a name="parameters"></a><span data-ttu-id="e70ca-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e70ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e70ca-108">*asciiText* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e70ca-108">*asciiText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70ca-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e70ca-109">Type: **string**</span></span>

<span data-ttu-id="e70ca-110">A série de caracteres ASCII ou Unicode a serem digitados.</span><span class="sxs-lookup"><span data-stu-id="e70ca-110">The series of ASCII or Unicode characters to type.</span></span> <span data-ttu-id="e70ca-111">O comprimento máximo dessa cadeia de caracteres depende do tipo de caracteres na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e70ca-111">The maximum length of this string depends on the type of characters in the string.</span></span>



| <span data-ttu-id="e70ca-112">Tipo de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="e70ca-112">String type</span></span>        | <span data-ttu-id="e70ca-113">Máximo de caracteres</span><span class="sxs-lookup"><span data-stu-id="e70ca-113">Maximum characters</span></span>                                                               |
|--------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e70ca-114">ASCII</span><span class="sxs-lookup"><span data-stu-id="e70ca-114">ASCII</span></span><br/>   | <span data-ttu-id="e70ca-115">512</span><span class="sxs-lookup"><span data-stu-id="e70ca-115">512</span></span><br/>                                                                   |
| <span data-ttu-id="e70ca-116">Unicode</span><span class="sxs-lookup"><span data-stu-id="e70ca-116">Unicode</span></span><br/> | <span data-ttu-id="e70ca-117">256 a 512, dependendo do número de pares substitutos na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e70ca-117">256 to 512, depending on the number of surrogate pairs in the string.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e70ca-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e70ca-118">Return value</span></span>

<span data-ttu-id="e70ca-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e70ca-119">Type: **uint32**</span></span>

<span data-ttu-id="e70ca-120">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="e70ca-120">A return value of zero indicates success.</span></span> <span data-ttu-id="e70ca-121">Um valor de retorno de um indica uma falha causada por caracteres não traduzível na cadeia de caracteres de entrada.</span><span class="sxs-lookup"><span data-stu-id="e70ca-121">A return value of one indicates a failure caused by nontranslatable characters in the input string.</span></span> <span data-ttu-id="e70ca-122">Todos os outros valores diferentes de zero indicam uma falha ao modificar o estado da chave.</span><span class="sxs-lookup"><span data-stu-id="e70ca-122">All other nonzero values indicate a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="e70ca-123">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e70ca-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e70ca-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-125">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e70ca-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-126">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e70ca-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-127">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e70ca-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-128">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e70ca-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-129">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e70ca-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-130">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e70ca-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-131">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e70ca-131">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-132">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e70ca-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-133">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e70ca-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-134">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e70ca-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e70ca-135">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e70ca-135">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e70ca-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="e70ca-136">Remarks</span></span>

<span data-ttu-id="e70ca-137">O acesso à classe de [**\_ teclado Msvm**](msvm-keyboard.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="e70ca-137">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e70ca-138">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e70ca-138">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="e70ca-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e70ca-139">Examples</span></span>

<span data-ttu-id="e70ca-140">O exemplo de C# a seguir simula a digitação de texto.</span><span class="sxs-lookup"><span data-stu-id="e70ca-140">The following C# sample simulates typing text.</span></span> <span data-ttu-id="e70ca-141">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="e70ca-141">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class TypeTextClass
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

        static void TypeText(string vmName, string text)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("TypeText");

            inParams["asciiText"] = text;

            ManagementBaseObject outParams = keyboard.InvokeMethod("TypeText", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Text {0} was typed on {1}", text, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to type '{0}' on {1}", text, vm["ElementName"]);
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
                Console.WriteLine("Usage: TypeText vmName Text");
                return;
            }
            TypeText(args[0], args[1]);
        }
    }
}

```



<span data-ttu-id="e70ca-142">O exemplo a seguir Visual Basic Scripting Edition (VBScript) simula a digitação de texto.</span><span class="sxs-lookup"><span data-stu-id="e70ca-142">The following Visual Basic Scripting Edition (VBScript) sample simulates typing text.</span></span>


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
    dim computer, objArgs, vmName, computerSystem, text, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       text = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript TypeText.vbs vmName text"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if TypeText(keyboard, text) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "TypeText operation failed"
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
' Type the given text to the given keyboard
'-----------------------------------------------------------------
Function TypeText(keyboard, text)
    WriteLog Format2("TypeText({0}, {1})", keyboard.ElementName, text)
    
    dim objInParam, objOutParams

    TypeText = false
    set objInParam = keyboard.Methods_("TypeText").InParameters.SpawnInstance_()
    objInParam.asciiText = text

    set objOutParams = keyboard.ExecMethod_("TypeText", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("'{0}' was typed on {1}", text, keyboard.ElementName)
        TypeText = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\Typetext.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="e70ca-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e70ca-143">Requirements</span></span>



| <span data-ttu-id="e70ca-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e70ca-144">Requirement</span></span> | <span data-ttu-id="e70ca-145">Valor</span><span class="sxs-lookup"><span data-stu-id="e70ca-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e70ca-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e70ca-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e70ca-147">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e70ca-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e70ca-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e70ca-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e70ca-149">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e70ca-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e70ca-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="e70ca-150">Namespace</span></span><br/>                | <span data-ttu-id="e70ca-151">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e70ca-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e70ca-152">MOF</span><span class="sxs-lookup"><span data-stu-id="e70ca-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e70ca-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e70ca-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e70ca-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e70ca-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e70ca-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e70ca-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e70ca-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="e70ca-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70ca-157">**\_Teclado Msvm**</span><span class="sxs-lookup"><span data-stu-id="e70ca-157">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

