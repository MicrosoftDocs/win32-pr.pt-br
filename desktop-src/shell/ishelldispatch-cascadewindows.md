---
description: Propaga todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar janelas em cascata.
ms.assetid: 6A957D70-D6A3-4485-8DF3-7FD2C6DEFF78
title: Método IShellDispatch. CascadeWindows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4252e4df579bc73e9f082630f9f98b83e3b57f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090846"
---
# <a name="ishelldispatchcascadewindows-method"></a><span data-ttu-id="8f3bb-104">Método IShellDispatch. CascadeWindows</span><span class="sxs-lookup"><span data-stu-id="8f3bb-104">IShellDispatch.CascadeWindows method</span></span>

<span data-ttu-id="8f3bb-105">Propaga todas as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f3bb-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="8f3bb-106">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **janelas em cascata**.</span><span class="sxs-lookup"><span data-stu-id="8f3bb-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3bb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f3bb-107">Syntax</span></span>


```JScript
IShellDispatch.CascadeWindows()
```


```VB

IShellDispatch.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="8f3bb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f3bb-108">Parameters</span></span>

<span data-ttu-id="8f3bb-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8f3bb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f3bb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f3bb-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="8f3bb-111">JScript</span><span class="sxs-lookup"><span data-stu-id="8f3bb-111">JScript</span></span>

<span data-ttu-id="8f3bb-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8f3bb-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="8f3bb-113">VB</span><span class="sxs-lookup"><span data-stu-id="8f3bb-113">VB</span></span>

<span data-ttu-id="8f3bb-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8f3bb-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f3bb-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f3bb-115">Remarks</span></span>

<span data-ttu-id="8f3bb-116">Esse método é implementado e acessado por meio do método [**shell. CascadeWindows**](shell-cascadewindows.md) .</span><span class="sxs-lookup"><span data-stu-id="8f3bb-116">This method is implemented and accessed through the [**Shell.CascadeWindows**](shell-cascadewindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="8f3bb-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f3bb-117">Examples</span></span>

<span data-ttu-id="8f3bb-118">Os exemplos a seguir mostram o uso de **CascadeWindows** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8f3bb-118">The following examples show the use of **CascadeWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8f3bb-119">JScript</span><span class="sxs-lookup"><span data-stu-id="8f3bb-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="8f3bb-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="8f3bb-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="8f3bb-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8f3bb-121">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8f3bb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f3bb-122">Requirements</span></span>



| <span data-ttu-id="8f3bb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f3bb-123">Requirement</span></span> | <span data-ttu-id="8f3bb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8f3bb-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3bb-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f3bb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8f3bb-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8f3bb-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8f3bb-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f3bb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8f3bb-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8f3bb-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8f3bb-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8f3bb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f3bb-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f3bb-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8f3bb-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="8f3bb-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8f3bb-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8f3bb-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8f3bb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8f3bb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f3bb-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8f3bb-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




