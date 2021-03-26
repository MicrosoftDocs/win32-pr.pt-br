---
description: Exibe a janela de ajuda e suporte do Windows. Esse método tem o mesmo efeito que clicar no menu iniciar e selecionar ajuda e suporte.
ms.assetid: 9460C87E-6703-4df6-A84C-8D394E0E6703
title: Método IShellDispatch. Help (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b58bcc97748cecf6ab4064ecccf3ba5bbe190b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967537"
---
# <a name="ishelldispatchhelp-method"></a><span data-ttu-id="4b598-104">Método IShellDispatch. Help</span><span class="sxs-lookup"><span data-stu-id="4b598-104">IShellDispatch.Help method</span></span>

<span data-ttu-id="4b598-105">Exibe a janela de ajuda e suporte do Windows.</span><span class="sxs-lookup"><span data-stu-id="4b598-105">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="4b598-106">Esse método tem o mesmo efeito que clicar no menu **Iniciar** e selecionar **ajuda e suporte**.</span><span class="sxs-lookup"><span data-stu-id="4b598-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b598-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b598-107">Syntax</span></span>


```JScript
IShellDispatch.Help()
```


```VB

IShellDispatch.Help()
```





## <a name="parameters"></a><span data-ttu-id="4b598-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b598-108">Parameters</span></span>

<span data-ttu-id="4b598-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b598-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b598-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b598-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="4b598-111">JScript</span><span class="sxs-lookup"><span data-stu-id="4b598-111">JScript</span></span>

<span data-ttu-id="4b598-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4b598-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="4b598-113">VB</span><span class="sxs-lookup"><span data-stu-id="4b598-113">VB</span></span>

<span data-ttu-id="4b598-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4b598-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b598-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b598-115">Remarks</span></span>

<span data-ttu-id="4b598-116">Esse método é implementado e acessado por meio do método [**shell. Help**](shell-help.md) .</span><span class="sxs-lookup"><span data-stu-id="4b598-116">This method is implemented and accessed through the [**Shell.Help**](shell-help.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="4b598-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b598-117">Examples</span></span>

<span data-ttu-id="4b598-118">Os exemplos a seguir mostram o uso da **ajuda** no JScript, no VBScript e no Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4b598-118">The following examples show the use of **Help** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4b598-119">JScript</span><span class="sxs-lookup"><span data-stu-id="4b598-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Help();
    }
</script>
```



<span data-ttu-id="4b598-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="4b598-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="4b598-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4b598-121">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4b598-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b598-122">Requirements</span></span>



| <span data-ttu-id="4b598-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b598-123">Requirement</span></span> | <span data-ttu-id="4b598-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4b598-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b598-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b598-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4b598-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4b598-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4b598-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b598-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4b598-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4b598-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4b598-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4b598-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b598-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b598-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4b598-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="4b598-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b598-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b598-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4b598-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4b598-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b598-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4b598-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




