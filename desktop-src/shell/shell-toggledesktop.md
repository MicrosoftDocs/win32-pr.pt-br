---
description: Método Shell. ToggleDesktop – exibe ou oculta a área de trabalho.
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
ms.openlocfilehash: c0d6c1e03db960c6abc8abc28ba8e79755fce639
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083674"
---
# <a name="shelltoggledesktop-method"></a><span data-ttu-id="fffde-103">Método Shell. ToggleDesktop</span><span class="sxs-lookup"><span data-stu-id="fffde-103">Shell.ToggleDesktop method</span></span>

<span data-ttu-id="fffde-104">Exibe ou oculta a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fffde-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="fffde-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fffde-105">Syntax</span></span>


```JScript
Shell.ToggleDesktop()
```


```VB

Shell.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="fffde-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fffde-106">Parameters</span></span>

<span data-ttu-id="fffde-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fffde-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fffde-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fffde-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fffde-109">JScript</span><span class="sxs-lookup"><span data-stu-id="fffde-109">JScript</span></span>

<span data-ttu-id="fffde-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fffde-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="fffde-111">VB</span><span class="sxs-lookup"><span data-stu-id="fffde-111">VB</span></span>

<span data-ttu-id="fffde-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fffde-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fffde-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fffde-113">Remarks</span></span>

<span data-ttu-id="fffde-114">Esse método tem o mesmo efeito que o botão **Mostrar área de trabalho** na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="fffde-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="fffde-115">Ele oculta todas as janelas abertas para mostrar a área de trabalho ou oculta a área de trabalho mostrando todas as janelas abertas.</span><span class="sxs-lookup"><span data-stu-id="fffde-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="fffde-116">O método **ToggleDesktop** não exibe uma interface do usuário, apenas invoca a ação de alternância.</span><span class="sxs-lookup"><span data-stu-id="fffde-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="fffde-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fffde-117">Examples</span></span>

<span data-ttu-id="fffde-118">Os exemplos a seguir mostram o uso apropriado de **ToggleDesktop** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fffde-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fffde-119">JScript</span><span class="sxs-lookup"><span data-stu-id="fffde-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="fffde-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="fffde-120">VBScript:</span></span>


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



<span data-ttu-id="fffde-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="fffde-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fffde-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fffde-122">Requirements</span></span>



| <span data-ttu-id="fffde-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fffde-123">Requirement</span></span> | <span data-ttu-id="fffde-124">Valor</span><span class="sxs-lookup"><span data-stu-id="fffde-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fffde-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fffde-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fffde-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fffde-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="fffde-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fffde-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fffde-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fffde-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fffde-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fffde-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fffde-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fffde-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fffde-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="fffde-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fffde-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fffde-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fffde-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fffde-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fffde-134"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fffde-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




