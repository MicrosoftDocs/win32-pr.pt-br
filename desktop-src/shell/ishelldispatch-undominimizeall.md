---
description: Restaura todas as janelas da área de trabalho para o estado em que estavam antes do último comando MinimizeAll.
ms.assetid: 32BDE544-C4FF-4a64-99AF-F8960AEC4690
title: Método IShellDispatch. UndoMinimizeALL (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1b11fdd7a0a82a11baa20b0f3a63a31a8a46b701
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502082"
---
# <a name="ishelldispatchundominimizeall-method"></a><span data-ttu-id="bd449-103">Método IShellDispatch. UndoMinimizeALL</span><span class="sxs-lookup"><span data-stu-id="bd449-103">IShellDispatch.UndoMinimizeALL method</span></span>

<span data-ttu-id="bd449-104">Restaura todas as janelas da área de trabalho para o estado em que estavam antes do último comando [**MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="bd449-104">Restores all desktop windows to the state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="bd449-105">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **desfazer minimizar todas as janelas** (em sistemas mais antigos) ou um segundo clique no ícone **Mostrar área de trabalho** na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bd449-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** (on older systems) or a second clicking of the **Show Desktop** icon in the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd449-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd449-106">Syntax</span></span>


```JScript
IShellDispatch.UndoMinimizeALL()
```


```VB

IShellDispatch.UndoMinimizeALL()
```





## <a name="parameters"></a><span data-ttu-id="bd449-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd449-107">Parameters</span></span>

<span data-ttu-id="bd449-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bd449-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd449-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd449-109">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="bd449-110">JScript</span><span class="sxs-lookup"><span data-stu-id="bd449-110">JScript</span></span>

<span data-ttu-id="bd449-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bd449-111">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="bd449-112">VB</span><span class="sxs-lookup"><span data-stu-id="bd449-112">VB</span></span>

<span data-ttu-id="bd449-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bd449-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd449-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd449-114">Remarks</span></span>

<span data-ttu-id="bd449-115">Esse método é implementado e acessado por meio do método [**shell. UndoMinimizeAll**](./shell-undominimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="bd449-115">This method is implemented and accessed through the [**Shell.UndoMinimizeAll**](./shell-undominimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="bd449-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bd449-116">Examples</span></span>

<span data-ttu-id="bd449-117">Os exemplos a seguir mostram o uso de **UndoMinimizeALL** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bd449-117">The following examples show the use of **UndoMinimizeALL** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bd449-118">JScript</span><span class="sxs-lookup"><span data-stu-id="bd449-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="bd449-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="bd449-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="bd449-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="bd449-120">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bd449-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd449-121">Requirements</span></span>



| <span data-ttu-id="bd449-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd449-122">Requirement</span></span> | <span data-ttu-id="bd449-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bd449-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd449-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd449-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bd449-125">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bd449-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bd449-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd449-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bd449-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bd449-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bd449-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bd449-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd449-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd449-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bd449-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="bd449-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bd449-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd449-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bd449-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bd449-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd449-133"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="bd449-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
