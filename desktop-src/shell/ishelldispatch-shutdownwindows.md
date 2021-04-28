---
description: Método IShellDispatch. ShutdownWindows – exibe a caixa de diálogo desligar o Windows. Isso é o mesmo que clicar no menu iniciar e selecionar desligar.
ms.assetid: 3C4F6579-6398-4af4-8911-FE22555B0ABC
title: Método IShellDispatch. ShutdownWindows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5146e17d17ba0f082ad2d80f91ae05c176cf44ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100464"
---
# <a name="ishelldispatchshutdownwindows-method"></a><span data-ttu-id="f19f8-104">Método IShellDispatch. ShutdownWindows</span><span class="sxs-lookup"><span data-stu-id="f19f8-104">IShellDispatch.ShutdownWindows method</span></span>

<span data-ttu-id="f19f8-105">Exibe a caixa de diálogo **desligar o Windows** .</span><span class="sxs-lookup"><span data-stu-id="f19f8-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="f19f8-106">Isso é o mesmo que clicar no menu **Iniciar** e selecionar **desligar**.</span><span class="sxs-lookup"><span data-stu-id="f19f8-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f19f8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f19f8-107">Syntax</span></span>


```JScript
IShellDispatch.ShutdownWindows()
```


```VB

IShellDispatch.ShutdownWindows()
```





## <a name="parameters"></a><span data-ttu-id="f19f8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f19f8-108">Parameters</span></span>

<span data-ttu-id="f19f8-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f19f8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f19f8-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f19f8-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f19f8-111">JScript</span><span class="sxs-lookup"><span data-stu-id="f19f8-111">JScript</span></span>

<span data-ttu-id="f19f8-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f19f8-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f19f8-113">VB</span><span class="sxs-lookup"><span data-stu-id="f19f8-113">VB</span></span>

<span data-ttu-id="f19f8-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f19f8-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f19f8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f19f8-115">Remarks</span></span>

<span data-ttu-id="f19f8-116">Esse método é implementado e acessado por meio do método [**shell. ShutdownWindows**](shell-shutdownwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="f19f8-116">This method is implemented and accessed through the [**Shell.ShutdownWindows**](shell-shutdownwindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="f19f8-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f19f8-117">Examples</span></span>

<span data-ttu-id="f19f8-118">O exemplo a seguir mostra o uso de **ShutdownWindows** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f19f8-118">The following example shows the use of **ShutdownWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f19f8-119">JScript</span><span class="sxs-lookup"><span data-stu-id="f19f8-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="f19f8-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="f19f8-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.ShutdownWindows

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f19f8-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f19f8-121">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f19f8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f19f8-122">Requirements</span></span>



| <span data-ttu-id="f19f8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f19f8-123">Requirement</span></span> | <span data-ttu-id="f19f8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f19f8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f19f8-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f19f8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f19f8-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f19f8-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f19f8-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f19f8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f19f8-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f19f8-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f19f8-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f19f8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f19f8-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f19f8-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f19f8-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="f19f8-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f19f8-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f19f8-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f19f8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f19f8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f19f8-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f19f8-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




