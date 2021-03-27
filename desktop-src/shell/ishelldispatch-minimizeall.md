---
description: Minimiza todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar minimizar todas as janelas em sistemas mais antigos ou clicar no ícone Mostrar área de trabalho na barra de tarefas.
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: Método IShellDispatch. MinimizeAll (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b8b8f20ab82a6216a03d772151f852fd9c69b917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502085"
---
# <a name="ishelldispatchminimizeall-method"></a><span data-ttu-id="fa54d-104">Método IShellDispatch. MinimizeAll</span><span class="sxs-lookup"><span data-stu-id="fa54d-104">IShellDispatch.MinimizeAll method</span></span>

<span data-ttu-id="fa54d-105">Minimiza todas as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fa54d-105">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="fa54d-106">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **minimizar todas as janelas** em sistemas mais antigos ou clicar no ícone **Mostrar área de trabalho** na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="fa54d-106">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon on the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa54d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa54d-107">Syntax</span></span>


```JScript
IShellDispatch.MinimizeAll()
```


```VB

IShellDispatch.MinimizeAll()
```





## <a name="parameters"></a><span data-ttu-id="fa54d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa54d-108">Parameters</span></span>

<span data-ttu-id="fa54d-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fa54d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa54d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa54d-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fa54d-111">JScript</span><span class="sxs-lookup"><span data-stu-id="fa54d-111">JScript</span></span>

<span data-ttu-id="fa54d-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fa54d-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="fa54d-113">VB</span><span class="sxs-lookup"><span data-stu-id="fa54d-113">VB</span></span>

<span data-ttu-id="fa54d-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fa54d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa54d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa54d-115">Remarks</span></span>

<span data-ttu-id="fa54d-116">Esse método é implementado e acessado por meio do método [**shell. MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="fa54d-116">This method is implemented and accessed through the [**Shell.MinimizeAll**](shell-minimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="fa54d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fa54d-117">Examples</span></span>

<span data-ttu-id="fa54d-118">Os exemplos a seguir mostram o uso de **MinimizeAll** em uso para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fa54d-118">The following examples show the use of **MinimizeAll** in use for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fa54d-119">JScript</span><span class="sxs-lookup"><span data-stu-id="fa54d-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="fa54d-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="fa54d-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="fa54d-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="fa54d-121">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fa54d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa54d-122">Requirements</span></span>



| <span data-ttu-id="fa54d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa54d-123">Requirement</span></span> | <span data-ttu-id="fa54d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="fa54d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa54d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa54d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa54d-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fa54d-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fa54d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa54d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa54d-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fa54d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa54d-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fa54d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa54d-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa54d-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="fa54d-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="fa54d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa54d-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa54d-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="fa54d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fa54d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa54d-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fa54d-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa54d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa54d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa54d-136">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="fa54d-136">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="fa54d-137">**UndoMinimizeALL**</span><span class="sxs-lookup"><span data-stu-id="fa54d-137">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




