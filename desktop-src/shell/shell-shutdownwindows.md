---
description: Método Shell. ShutdownWindows – exibe a caixa de diálogo desligar o Windows. Isso é o mesmo que clicar no menu iniciar e selecionar desligar.
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
ms.openlocfilehash: 2a3c0746caccb360f6f7f0156b72a57ed0a2d2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083664"
---
# <a name="shellshutdownwindows-method"></a><span data-ttu-id="9d4dc-104">Método Shell. ShutdownWindows</span><span class="sxs-lookup"><span data-stu-id="9d4dc-104">Shell.ShutdownWindows method</span></span>

<span data-ttu-id="9d4dc-105">Exibe a caixa de diálogo **desligar o Windows** .</span><span class="sxs-lookup"><span data-stu-id="9d4dc-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="9d4dc-106">Isso é o mesmo que clicar no menu **Iniciar** e selecionar **desligar**.</span><span class="sxs-lookup"><span data-stu-id="9d4dc-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d4dc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d4dc-107">Syntax</span></span>


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a><span data-ttu-id="9d4dc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d4dc-108">Parameters</span></span>

<span data-ttu-id="9d4dc-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9d4dc-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="9d4dc-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9d4dc-110">Examples</span></span>

<span data-ttu-id="9d4dc-111">O exemplo a seguir mostra **ShutdownWindows** em uso.</span><span class="sxs-lookup"><span data-stu-id="9d4dc-111">The following example shows **ShutdownWindows** in use.</span></span> <span data-ttu-id="9d4dc-112">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9d4dc-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9d4dc-113">JScript</span><span class="sxs-lookup"><span data-stu-id="9d4dc-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="9d4dc-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="9d4dc-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



<span data-ttu-id="9d4dc-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="9d4dc-115">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9d4dc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d4dc-116">Requirements</span></span>



| <span data-ttu-id="9d4dc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d4dc-117">Requirement</span></span> | <span data-ttu-id="9d4dc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4dc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4dc-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d4dc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9d4dc-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9d4dc-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9d4dc-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d4dc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9d4dc-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d4dc-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9d4dc-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9d4dc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d4dc-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d4dc-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9d4dc-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="9d4dc-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9d4dc-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d4dc-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9d4dc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9d4dc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d4dc-128"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9d4dc-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




