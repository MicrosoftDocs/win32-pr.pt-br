---
description: Cria e retorna um novo objeto ShellWindows que é uma cópia desse objeto ShellWindows.
title: Método de ShellWindows._NewEnum (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows._NewEnum
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 85e84c13-62aa-4502-b642-ca55273a800d
ms.openlocfilehash: ded5ae2c337e80359c012fb63a37aa13cc43b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171546"
---
# <a name="shellwindows_newenum-method"></a><span data-ttu-id="e22f8-103">ShellWindows. \_ Método NewEnum</span><span class="sxs-lookup"><span data-stu-id="e22f8-103">ShellWindows.\_NewEnum method</span></span>

<span data-ttu-id="e22f8-104">Cria e retorna um novo objeto [**ShellWindows**](shellwindows.md) que é uma cópia desse objeto **ShellWindows** .</span><span class="sxs-lookup"><span data-stu-id="e22f8-104">Creates and returns a new [**ShellWindows**](shellwindows.md) object that is a copy of this **ShellWindows** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e22f8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e22f8-105">Syntax</span></span>


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a><span data-ttu-id="e22f8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e22f8-106">Parameters</span></span>

<span data-ttu-id="e22f8-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e22f8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e22f8-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e22f8-108">Return value</span></span>

<span data-ttu-id="e22f8-109">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="e22f8-109">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="e22f8-110">Uma referência de objeto para a cópia do objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="e22f8-110">An object reference to the [**ShellWindows**](shellwindows.md) object copy.</span></span>

## <a name="examples"></a><span data-ttu-id="e22f8-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e22f8-111">Examples</span></span>

<span data-ttu-id="e22f8-112">O exemplo a seguir mostra o **\_ NewEnum** em uso.</span><span class="sxs-lookup"><span data-stu-id="e22f8-112">The following example shows **\_NewEnum** in use.</span></span> <span data-ttu-id="e22f8-113">O uso adequado é mostrado para o VBScript e o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e22f8-113">Proper usage is shown for VBScript and Visual Basic.</span></span> <span data-ttu-id="e22f8-114">Este método não pode ser usado com JScript.</span><span class="sxs-lookup"><span data-stu-id="e22f8-114">This method cannot be used with JScript.</span></span>

<span data-ttu-id="e22f8-115">VBScript</span><span class="sxs-lookup"><span data-stu-id="e22f8-115">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsNewEnumVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim objEnumItems
            
            for each objEnumItems in objShellWindows
                alert(objEnumItems.Type)
            next
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e22f8-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e22f8-116">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsNewEnumVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Dim vEnumItem As Variant
        
        For Each vEnumItem In objShellWindows
            Debug.Print vEnumItem.Type
        Next vEnumItem
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e22f8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e22f8-117">Requirements</span></span>



| <span data-ttu-id="e22f8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e22f8-118">Requirement</span></span> | <span data-ttu-id="e22f8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e22f8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e22f8-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e22f8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e22f8-121">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e22f8-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e22f8-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e22f8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e22f8-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e22f8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e22f8-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e22f8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e22f8-125"><dt>O textdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e22f8-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="e22f8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e22f8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e22f8-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e22f8-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
