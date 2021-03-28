---
description: Exibe o centro de ajuda e suporte do Windows. Esse método tem o mesmo efeito que clicar no menu iniciar e selecionar ajuda e suporte.
ms.assetid: fc13fef8-dac8-4c59-936d-8da0e63e06d4
title: Método Shell. Help (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bfb4e9b3272355c41d13526d2e526515ff65d42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169554"
---
# <a name="shellhelp-method"></a><span data-ttu-id="e7bf5-104">Método Shell. Help</span><span class="sxs-lookup"><span data-stu-id="e7bf5-104">Shell.Help method</span></span>

<span data-ttu-id="e7bf5-105">Exibe o centro de ajuda e suporte do Windows.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-105">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="e7bf5-106">Esse método tem o mesmo efeito que clicar no menu **Iniciar** e selecionar **ajuda e suporte**.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7bf5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7bf5-107">Syntax</span></span>


```JScript
Shell.Help()
```


```VB

Shell.Help()
```





## <a name="parameters"></a><span data-ttu-id="e7bf5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7bf5-108">Parameters</span></span>

<span data-ttu-id="e7bf5-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7bf5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7bf5-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e7bf5-111">JScript</span><span class="sxs-lookup"><span data-stu-id="e7bf5-111">JScript</span></span>

<span data-ttu-id="e7bf5-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="e7bf5-113">VB</span><span class="sxs-lookup"><span data-stu-id="e7bf5-113">VB</span></span>

<span data-ttu-id="e7bf5-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="e7bf5-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e7bf5-115">Examples</span></span>

<span data-ttu-id="e7bf5-116">O exemplo a seguir mostra a **ajuda** em uso.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-116">The following example shows **Help** in use.</span></span> <span data-ttu-id="e7bf5-117">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e7bf5-118">JScript</span><span class="sxs-lookup"><span data-stu-id="e7bf5-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Help();
    }
</script>
```



<span data-ttu-id="e7bf5-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="e7bf5-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e7bf5-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e7bf5-120">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e7bf5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7bf5-121">Requirements</span></span>



| <span data-ttu-id="e7bf5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7bf5-122">Requirement</span></span> | <span data-ttu-id="e7bf5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e7bf5-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7bf5-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7bf5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e7bf5-125">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e7bf5-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e7bf5-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7bf5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e7bf5-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7bf5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e7bf5-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e7bf5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7bf5-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7bf5-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e7bf5-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="e7bf5-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e7bf5-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7bf5-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e7bf5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e7bf5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7bf5-133"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e7bf5-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




