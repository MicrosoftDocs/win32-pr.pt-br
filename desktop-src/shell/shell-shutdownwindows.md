---
description: Exibe a caixa de diálogo desligar o Windows. Isso é o mesmo que clicar no menu iniciar e selecionar desligar.
ms.assetid: 6fa8e2e0-a58f-4837-89f5-898cece2d80a
title: Método Shell. ShutdownWindows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 804a1e211e191206d20f83d85dee2202492bfd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170086"
---
# <a name="shellshutdownwindows-method"></a><span data-ttu-id="e9797-104">Método Shell. ShutdownWindows</span><span class="sxs-lookup"><span data-stu-id="e9797-104">Shell.ShutdownWindows method</span></span>

<span data-ttu-id="e9797-105">Exibe a caixa de diálogo **desligar o Windows** .</span><span class="sxs-lookup"><span data-stu-id="e9797-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="e9797-106">Isso é o mesmo que clicar no menu **Iniciar** e selecionar **desligar**.</span><span class="sxs-lookup"><span data-stu-id="e9797-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9797-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9797-107">Syntax</span></span>


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a><span data-ttu-id="e9797-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9797-108">Parameters</span></span>

<span data-ttu-id="e9797-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e9797-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="e9797-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e9797-110">Examples</span></span>

<span data-ttu-id="e9797-111">O exemplo a seguir mostra **ShutdownWindows** em uso.</span><span class="sxs-lookup"><span data-stu-id="e9797-111">The following example shows **ShutdownWindows** in use.</span></span> <span data-ttu-id="e9797-112">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e9797-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e9797-113">JScript</span><span class="sxs-lookup"><span data-stu-id="e9797-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="e9797-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="e9797-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



<span data-ttu-id="e9797-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e9797-115">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e9797-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9797-116">Requirements</span></span>



| <span data-ttu-id="e9797-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9797-117">Requirement</span></span> | <span data-ttu-id="e9797-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e9797-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9797-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9797-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e9797-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e9797-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e9797-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9797-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e9797-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e9797-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e9797-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e9797-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9797-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9797-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e9797-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="e9797-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e9797-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e9797-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e9797-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e9797-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9797-128"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e9797-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




