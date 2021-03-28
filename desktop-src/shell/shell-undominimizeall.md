---
description: Restaura todas as janelas da área de trabalho para o mesmo estado em que estavam antes do último comando MinimizeAll.
ms.assetid: dcedfa18-6dde-4fb8-9679-4d6ff80249e4
title: Método Shell. UndoMinimizeALL (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a5010e4ac6b4fca42689f7c80db50c55ab2cb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170083"
---
# <a name="shellundominimizeall-method"></a><span data-ttu-id="5ccc7-103">Método Shell. UndoMinimizeALL</span><span class="sxs-lookup"><span data-stu-id="5ccc7-103">Shell.UndoMinimizeALL method</span></span>

<span data-ttu-id="5ccc7-104">Restaura todas as janelas da área de trabalho para o mesmo estado em que estavam antes do último comando [**MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="5ccc7-104">Restores all desktop windows to the same state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="5ccc7-105">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **desfazer minimizar todas as janelas** em sistemas mais antigos ou um segundo clique no ícone **Mostrar área de trabalho** na área início rápido da barra de tarefas no Windows 2000 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5ccc7-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** on older systems or a second clicking of the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ccc7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ccc7-106">Syntax</span></span>


```JScript
iRetVal = Shell.UndoMinimizeALL()
```


```VB

Shell.UndoMinimizeALL() As Integer
```





## <a name="parameters"></a><span data-ttu-id="5ccc7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ccc7-107">Parameters</span></span>

<span data-ttu-id="5ccc7-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5ccc7-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="5ccc7-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5ccc7-109">Examples</span></span>

<span data-ttu-id="5ccc7-110">O exemplo a seguir mostra **UndoMinimizeALL** em uso.</span><span class="sxs-lookup"><span data-stu-id="5ccc7-110">The following example shows **UndoMinimizeALL** in use.</span></span> <span data-ttu-id="5ccc7-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5ccc7-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5ccc7-112">JScript</span><span class="sxs-lookup"><span data-stu-id="5ccc7-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="5ccc7-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="5ccc7-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="5ccc7-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5ccc7-114">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5ccc7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ccc7-115">Requirements</span></span>



| <span data-ttu-id="5ccc7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ccc7-116">Requirement</span></span> | <span data-ttu-id="5ccc7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5ccc7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ccc7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ccc7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5ccc7-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5ccc7-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5ccc7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ccc7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5ccc7-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5ccc7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ccc7-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5ccc7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ccc7-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ccc7-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5ccc7-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="5ccc7-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ccc7-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ccc7-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5ccc7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5ccc7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ccc7-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5ccc7-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




