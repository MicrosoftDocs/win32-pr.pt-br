---
description: Exibe a caixa de diálogo Propriedades de data e hora. Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar ajustar data/hora.
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: Método Shell. setTime (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b610effe87bd9e4ab33a6e8396e90f79e7bbbe9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967953"
---
# <a name="shellsettime-method"></a><span data-ttu-id="970b0-104">Método Shell. setTime</span><span class="sxs-lookup"><span data-stu-id="970b0-104">Shell.SetTime method</span></span>

<span data-ttu-id="970b0-105">Exibe a caixa de diálogo **Propriedades de data e hora** .</span><span class="sxs-lookup"><span data-stu-id="970b0-105">Displays the **Date and Time Properties** dialog box.</span></span> <span data-ttu-id="970b0-106">Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar **Ajustar data/hora**.</span><span class="sxs-lookup"><span data-stu-id="970b0-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust Date/Time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="970b0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="970b0-107">Syntax</span></span>


```JScript
iRetVal = Shell.SetTime()
```


```VB

Shell.SetTime() As Integer
```





## <a name="parameters"></a><span data-ttu-id="970b0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="970b0-108">Parameters</span></span>

<span data-ttu-id="970b0-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="970b0-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="970b0-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="970b0-110">Examples</span></span>

<span data-ttu-id="970b0-111">O exemplo a seguir mostra **setTime** em uso.</span><span class="sxs-lookup"><span data-stu-id="970b0-111">The following example shows **SetTime** in use.</span></span> <span data-ttu-id="970b0-112">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="970b0-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="970b0-113">JScript</span><span class="sxs-lookup"><span data-stu-id="970b0-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



<span data-ttu-id="970b0-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="970b0-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.SetTime
 
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="970b0-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="970b0-115">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.SetTime
 
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="970b0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="970b0-116">Requirements</span></span>



| <span data-ttu-id="970b0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="970b0-117">Requirement</span></span> | <span data-ttu-id="970b0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="970b0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="970b0-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="970b0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="970b0-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="970b0-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="970b0-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="970b0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="970b0-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="970b0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="970b0-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="970b0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="970b0-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="970b0-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="970b0-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="970b0-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="970b0-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="970b0-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="970b0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="970b0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="970b0-128"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="970b0-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




