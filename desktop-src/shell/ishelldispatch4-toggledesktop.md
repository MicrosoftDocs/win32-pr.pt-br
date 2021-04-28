---
description: Método IShellDispatch4. ToggleDesktop – exibe ou oculta a área de trabalho.
title: Método IShellDispatch4. ToggleDesktop (shldisp. h)
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
ms.openlocfilehash: b635408ed8a44b8bb0d27e52c167470f80f61b18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116814"
---
# <a name="ishelldispatch4toggledesktop-method"></a><span data-ttu-id="38956-103">Método IShellDispatch4. ToggleDesktop</span><span class="sxs-lookup"><span data-stu-id="38956-103">IShellDispatch4.ToggleDesktop method</span></span>

<span data-ttu-id="38956-104">Exibe ou oculta a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="38956-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="38956-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38956-105">Syntax</span></span>


```JScript
IShellDispatch4.ToggleDesktop()
```


```VB

IShellDispatch4.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="38956-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38956-106">Parameters</span></span>

<span data-ttu-id="38956-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="38956-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38956-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="38956-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="38956-109">JScript</span><span class="sxs-lookup"><span data-stu-id="38956-109">JScript</span></span>

<span data-ttu-id="38956-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="38956-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="38956-111">VB</span><span class="sxs-lookup"><span data-stu-id="38956-111">VB</span></span>

<span data-ttu-id="38956-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="38956-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38956-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="38956-113">Remarks</span></span>

<span data-ttu-id="38956-114">Esse método tem o mesmo efeito que o botão **Mostrar área de trabalho** na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="38956-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="38956-115">Ele oculta todas as janelas abertas para mostrar a área de trabalho ou oculta a área de trabalho mostrando todas as janelas abertas.</span><span class="sxs-lookup"><span data-stu-id="38956-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="38956-116">O método **ToggleDesktop** não exibe uma interface do usuário, apenas invoca a ação de alternância.</span><span class="sxs-lookup"><span data-stu-id="38956-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="38956-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="38956-117">Examples</span></span>

<span data-ttu-id="38956-118">Os exemplos a seguir mostram o uso apropriado de **ToggleDesktop** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="38956-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="38956-119">JScript</span><span class="sxs-lookup"><span data-stu-id="38956-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="38956-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="38956-120">VBScript:</span></span>


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



<span data-ttu-id="38956-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="38956-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="38956-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38956-122">Requirements</span></span>



| <span data-ttu-id="38956-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="38956-123">Requirement</span></span> | <span data-ttu-id="38956-124">Valor</span><span class="sxs-lookup"><span data-stu-id="38956-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38956-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38956-125">Minimum supported client</span></span><br/> | <span data-ttu-id="38956-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="38956-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="38956-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38956-127">Minimum supported server</span></span><br/> | <span data-ttu-id="38956-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="38956-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="38956-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38956-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="38956-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="38956-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="38956-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="38956-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38956-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38956-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="38956-133">DLL</span><span class="sxs-lookup"><span data-stu-id="38956-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38956-134"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="38956-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




