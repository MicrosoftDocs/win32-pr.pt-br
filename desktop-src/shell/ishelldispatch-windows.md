---
description: Cria e retorna um objeto ShellWindows. Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao shell.
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: Método IShellDispatch. Windows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cb5f84caebf38deb27c7fb60565167793fead561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647544"
---
# <a name="ishelldispatchwindows-method"></a><span data-ttu-id="54a03-104">Método IShellDispatch. Windows</span><span class="sxs-lookup"><span data-stu-id="54a03-104">IShellDispatch.Windows method</span></span>

<span data-ttu-id="54a03-105">Cria e retorna um objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="54a03-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="54a03-106">Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao shell.</span><span class="sxs-lookup"><span data-stu-id="54a03-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="54a03-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54a03-107">Syntax</span></span>


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="54a03-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54a03-108">Parameters</span></span>

<span data-ttu-id="54a03-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="54a03-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54a03-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="54a03-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="54a03-111">JScript</span><span class="sxs-lookup"><span data-stu-id="54a03-111">JScript</span></span>

<span data-ttu-id="54a03-112">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="54a03-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="54a03-113">Uma referência de objeto para o objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="54a03-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="54a03-114">VB</span><span class="sxs-lookup"><span data-stu-id="54a03-114">VB</span></span>

<span data-ttu-id="54a03-115">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="54a03-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="54a03-116">Uma referência de objeto para o objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="54a03-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="54a03-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="54a03-117">Remarks</span></span>

<span data-ttu-id="54a03-118">Esse método é implementado e acessado por meio do método [**shell. Windows**](shell-windows.md) .</span><span class="sxs-lookup"><span data-stu-id="54a03-118">This method is implemented and accessed through the [**Shell.Windows**](shell-windows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="54a03-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="54a03-119">Examples</span></span>

<span data-ttu-id="54a03-120">Os exemplos a seguir usam o **Windows** para recuperar o objeto [**ShellWindows**](shellwindows.md) e exibir uma contagem do número de itens que ele contém.</span><span class="sxs-lookup"><span data-stu-id="54a03-120">The following examples use **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="54a03-121">O uso é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="54a03-121">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="54a03-122">JScript</span><span class="sxs-lookup"><span data-stu-id="54a03-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();

        if (objShellWindows != null)
        {
            alert(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="54a03-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="54a03-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows

        if (not objShellWindows is nothing) then
            alert(objShellWindows.Count)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="54a03-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="54a03-124">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="54a03-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54a03-125">Requirements</span></span>



| <span data-ttu-id="54a03-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="54a03-126">Requirement</span></span> | <span data-ttu-id="54a03-127">Valor</span><span class="sxs-lookup"><span data-stu-id="54a03-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54a03-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54a03-128">Minimum supported client</span></span><br/> | <span data-ttu-id="54a03-129">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="54a03-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="54a03-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54a03-130">Minimum supported server</span></span><br/> | <span data-ttu-id="54a03-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="54a03-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="54a03-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="54a03-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="54a03-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="54a03-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="54a03-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="54a03-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54a03-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54a03-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="54a03-136">DLL</span><span class="sxs-lookup"><span data-stu-id="54a03-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54a03-137"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="54a03-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
