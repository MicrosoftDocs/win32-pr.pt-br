---
description: Método IShellDispatch4.ToggleDesktop – exibe ou oculta a área de trabalho.
title: Método IShellDispatch4.ToggleDesktop (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 60199e18-b8da-48a6-b316-e7f07ff44b78
ms.openlocfilehash: e78c14e2aa7f918ff27b21bdab0ce71bed08a84a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840927"
---
# <a name="ishelldispatch4toggledesktop-method"></a><span data-ttu-id="ae963-103">Método IShellDispatch4.ToggleDesktop</span><span class="sxs-lookup"><span data-stu-id="ae963-103">IShellDispatch4.ToggleDesktop method</span></span>

<span data-ttu-id="ae963-104">Exibe ou oculta a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ae963-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae963-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae963-105">Syntax</span></span>


```JScript
IShellDispatch4.ToggleDesktop()
```


```VB

IShellDispatch4.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="ae963-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae963-106">Parameters</span></span>

<span data-ttu-id="ae963-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ae963-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae963-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae963-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ae963-109">JScript</span><span class="sxs-lookup"><span data-stu-id="ae963-109">JScript</span></span>

<span data-ttu-id="ae963-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ae963-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="ae963-111">VB</span><span class="sxs-lookup"><span data-stu-id="ae963-111">VB</span></span>

<span data-ttu-id="ae963-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ae963-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae963-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae963-113">Remarks</span></span>

<span data-ttu-id="ae963-114">Esse método tem o mesmo efeito que o **botão Mostrar Área** de Trabalho na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="ae963-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="ae963-115">Ele oculta todas as janelas abertas para mostrar a área de trabalho ou oculta a área de trabalho mostrando todas as janelas abertas.</span><span class="sxs-lookup"><span data-stu-id="ae963-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="ae963-116">O **método ToggleDesktop** não exibe uma interface do usuário, apenas invoca a ação de alternância.</span><span class="sxs-lookup"><span data-stu-id="ae963-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="ae963-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ae963-117">Examples</span></span>

<span data-ttu-id="ae963-118">Os exemplos a seguir mostram o uso adequado de **ToggleDesktop** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ae963-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ae963-119">Jscript:</span><span class="sxs-lookup"><span data-stu-id="ae963-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="ae963-120">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="ae963-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4ToggleDesktopVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.ToggleDesktop
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ae963-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ae963-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ae963-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae963-122">Requirements</span></span>



| <span data-ttu-id="ae963-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae963-123">Requirement</span></span> | <span data-ttu-id="ae963-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ae963-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae963-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae963-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ae963-126">Somente \[ aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ae963-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ae963-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae963-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ae963-128">Somente aplicativos da área de trabalho do Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae963-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ae963-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae963-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae963-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ae963-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ae963-131">Idl</span><span class="sxs-lookup"><span data-stu-id="ae963-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ae963-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae963-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ae963-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ae963-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae963-134"><dt>Shell32.dll (versão 6.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ae963-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




