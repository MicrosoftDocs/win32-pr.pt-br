---
description: Método Shell. Windows – cria e retorna um objeto ShellWindows. Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao shell.
title: Método Shell. Windows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ffa6311c-8bbe-45c4-9b06-069779d2306d
ms.openlocfilehash: d46e27781dc569b473615926509f51ed9d089af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104064"
---
# <a name="shellwindows-method"></a><span data-ttu-id="8b299-104">Método Shell. Windows</span><span class="sxs-lookup"><span data-stu-id="8b299-104">Shell.Windows method</span></span>

<span data-ttu-id="8b299-105">Cria e retorna um objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="8b299-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="8b299-106">Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao shell.</span><span class="sxs-lookup"><span data-stu-id="8b299-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b299-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b299-107">Syntax</span></span>


```JScript
retVal = Shell.Windows()
```


```VB

Shell.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="8b299-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b299-108">Parameters</span></span>

<span data-ttu-id="8b299-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8b299-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b299-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8b299-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="8b299-111">JScript</span><span class="sxs-lookup"><span data-stu-id="8b299-111">JScript</span></span>

<span data-ttu-id="8b299-112">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="8b299-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="8b299-113">Uma referência de objeto para o objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="8b299-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="8b299-114">VB</span><span class="sxs-lookup"><span data-stu-id="8b299-114">VB</span></span>

<span data-ttu-id="8b299-115">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="8b299-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="8b299-116">Uma referência de objeto para o objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="8b299-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="8b299-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8b299-117">Examples</span></span>

<span data-ttu-id="8b299-118">O exemplo a seguir usa o **Windows** para recuperar o objeto [**ShellWindows**](shellwindows.md) e exibir uma contagem do número de itens que ele contém.</span><span class="sxs-lookup"><span data-stu-id="8b299-118">The following example uses **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="8b299-119">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8b299-119">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8b299-120">JScript</span><span class="sxs-lookup"><span data-stu-id="8b299-120">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objShell.Windows();

        if (objShellWindows != null)
        {
            var Shell = new ActiveXObject("WScript.Shell");
            Shell.Popup(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="8b299-121">VBScript</span><span class="sxs-lookup"><span data-stu-id="8b299-121">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVBS()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objShell.Windows

        if (not objShellWindows is nothing) then
            WScript.Echo objShellWindows.Count
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="8b299-122">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8b299-122">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objShell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8b299-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b299-123">Requirements</span></span>



| <span data-ttu-id="8b299-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b299-124">Requirement</span></span> | <span data-ttu-id="8b299-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8b299-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b299-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b299-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8b299-127">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8b299-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8b299-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b299-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8b299-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8b299-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8b299-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8b299-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b299-131"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b299-131"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8b299-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="8b299-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8b299-133"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b299-133"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8b299-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8b299-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b299-135"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8b299-135"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
