---
description: Propaga todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar janelas em cascata.
ms.assetid: f73d2066-4626-455b-8ee6-f7004cc9e699
title: Método Shell. CascadeWindows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 751182ec53e0495021f4a6e2fad355c2c700ad66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505982"
---
# <a name="shellcascadewindows-method"></a><span data-ttu-id="a806a-104">Método Shell. CascadeWindows</span><span class="sxs-lookup"><span data-stu-id="a806a-104">Shell.CascadeWindows method</span></span>

<span data-ttu-id="a806a-105">Propaga todas as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a806a-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="a806a-106">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **janelas em cascata**.</span><span class="sxs-lookup"><span data-stu-id="a806a-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade Windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a806a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a806a-107">Syntax</span></span>


```JScript
Shell.CascadeWindows()
```


```VB

Shell.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="a806a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a806a-108">Parameters</span></span>

<span data-ttu-id="a806a-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a806a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a806a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a806a-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a806a-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a806a-111">JScript</span></span>

<span data-ttu-id="a806a-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a806a-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a806a-113">VB</span><span class="sxs-lookup"><span data-stu-id="a806a-113">VB</span></span>

<span data-ttu-id="a806a-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a806a-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="a806a-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a806a-115">Examples</span></span>

<span data-ttu-id="a806a-116">O exemplo a seguir mostra **CascadeWindows** em uso.</span><span class="sxs-lookup"><span data-stu-id="a806a-116">The following example shows **CascadeWindows** in use.</span></span> <span data-ttu-id="a806a-117">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a806a-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a806a-118">JScript</span><span class="sxs-lookup"><span data-stu-id="a806a-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="a806a-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="a806a-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a806a-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a806a-120">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a806a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a806a-121">Requirements</span></span>



| <span data-ttu-id="a806a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a806a-122">Requirement</span></span> | <span data-ttu-id="a806a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a806a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a806a-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a806a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a806a-125">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a806a-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a806a-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a806a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a806a-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a806a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a806a-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a806a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a806a-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a806a-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a806a-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="a806a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a806a-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a806a-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a806a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a806a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a806a-133"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a806a-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




