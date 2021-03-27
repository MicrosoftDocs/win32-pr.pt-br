---
description: Exibe ou oculta a área de trabalho.
title: Método Shell. ToggleDesktop (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: BD07F7F2-A588-4189-95F4-3A8E2905E8F5
ms.openlocfilehash: 888723aeba8bd54c6ada659022286e4825e4067d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662440"
---
# <a name="shelltoggledesktop-method"></a><span data-ttu-id="17ee8-103">Método Shell. ToggleDesktop</span><span class="sxs-lookup"><span data-stu-id="17ee8-103">Shell.ToggleDesktop method</span></span>

<span data-ttu-id="17ee8-104">Exibe ou oculta a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="17ee8-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ee8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17ee8-105">Syntax</span></span>


```JScript
Shell.ToggleDesktop()
```


```VB

Shell.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="17ee8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17ee8-106">Parameters</span></span>

<span data-ttu-id="17ee8-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="17ee8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17ee8-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17ee8-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="17ee8-109">JScript</span><span class="sxs-lookup"><span data-stu-id="17ee8-109">JScript</span></span>

<span data-ttu-id="17ee8-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="17ee8-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="17ee8-111">VB</span><span class="sxs-lookup"><span data-stu-id="17ee8-111">VB</span></span>

<span data-ttu-id="17ee8-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="17ee8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17ee8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="17ee8-113">Remarks</span></span>

<span data-ttu-id="17ee8-114">Esse método tem o mesmo efeito que o botão **Mostrar área de trabalho** na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="17ee8-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="17ee8-115">Ele oculta todas as janelas abertas para mostrar a área de trabalho ou oculta a área de trabalho mostrando todas as janelas abertas.</span><span class="sxs-lookup"><span data-stu-id="17ee8-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="17ee8-116">O método **ToggleDesktop** não exibe uma interface do usuário, apenas invoca a ação de alternância.</span><span class="sxs-lookup"><span data-stu-id="17ee8-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="17ee8-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="17ee8-117">Examples</span></span>

<span data-ttu-id="17ee8-118">Os exemplos a seguir mostram o uso apropriado de **ToggleDesktop** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="17ee8-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="17ee8-119">JScript</span><span class="sxs-lookup"><span data-stu-id="17ee8-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="17ee8-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="17ee8-120">VBScript:</span></span>


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



<span data-ttu-id="17ee8-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="17ee8-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="17ee8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17ee8-122">Requirements</span></span>



| <span data-ttu-id="17ee8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="17ee8-123">Requirement</span></span> | <span data-ttu-id="17ee8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="17ee8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17ee8-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17ee8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="17ee8-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="17ee8-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="17ee8-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17ee8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="17ee8-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="17ee8-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="17ee8-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17ee8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="17ee8-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="17ee8-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="17ee8-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="17ee8-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17ee8-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17ee8-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="17ee8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="17ee8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17ee8-134"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="17ee8-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




