---
description: Minimiza todas as janelas na área de trabalho.
ms.assetid: 3af98a16-27d1-4c93-ac72-7c9e24e68c23
title: Método Shell. MinimizeAll (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 55b615cfed8813f5567b13d58648fef36aaedda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968168"
---
# <a name="shellminimizeall-method"></a><span data-ttu-id="cf6b9-103">Método Shell. MinimizeAll</span><span class="sxs-lookup"><span data-stu-id="cf6b9-103">Shell.MinimizeAll method</span></span>

<span data-ttu-id="cf6b9-104">Minimiza todas as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf6b9-104">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="cf6b9-105">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **minimizar todas as janelas** em sistemas mais antigos ou clicar no ícone **Mostrar área de trabalho** na área início rápido da barra de tarefas no Windows 2000 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cf6b9-105">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf6b9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf6b9-106">Syntax</span></span>


```JScript
iRetVal = Shell.MinimizeAll()
```


```VB

Shell.MinimizeAll() As Integer
```





## <a name="parameters"></a><span data-ttu-id="cf6b9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf6b9-107">Parameters</span></span>

<span data-ttu-id="cf6b9-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cf6b9-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="cf6b9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cf6b9-109">Examples</span></span>

<span data-ttu-id="cf6b9-110">O exemplo a seguir mostra **MinimizeAll** em uso.</span><span class="sxs-lookup"><span data-stu-id="cf6b9-110">The following example shows **MinimizeAll** in use.</span></span> <span data-ttu-id="cf6b9-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cf6b9-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cf6b9-112">JScript</span><span class="sxs-lookup"><span data-stu-id="cf6b9-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="cf6b9-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="cf6b9-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="cf6b9-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cf6b9-114">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cf6b9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf6b9-115">Requirements</span></span>



| <span data-ttu-id="cf6b9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf6b9-116">Requirement</span></span> | <span data-ttu-id="cf6b9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cf6b9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6b9-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf6b9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cf6b9-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cf6b9-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cf6b9-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf6b9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cf6b9-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf6b9-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cf6b9-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cf6b9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf6b9-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf6b9-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cf6b9-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="cf6b9-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cf6b9-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf6b9-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cf6b9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cf6b9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf6b9-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="cf6b9-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf6b9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf6b9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf6b9-129">**Shell**</span><span class="sxs-lookup"><span data-stu-id="cf6b9-129">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="cf6b9-130">**UndoMinimizeALL**</span><span class="sxs-lookup"><span data-stu-id="cf6b9-130">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




