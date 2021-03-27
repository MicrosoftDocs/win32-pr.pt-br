---
description: Exibe a caixa de diálogo Executar para o usuário.
ms.assetid: BC7C4C26-593D-4467-A2AA-4F2DF835C989
title: Método IShellDispatch. FileRun (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 56806edf06d334d90ad038886d955c00876f8f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647548"
---
# <a name="ishelldispatchfilerun-method"></a><span data-ttu-id="e74a3-103">Método IShellDispatch. FileRun</span><span class="sxs-lookup"><span data-stu-id="e74a3-103">IShellDispatch.FileRun method</span></span>

<span data-ttu-id="e74a3-104">Exibe a caixa de diálogo **executar** para o usuário.</span><span class="sxs-lookup"><span data-stu-id="e74a3-104">Displays the **Run** dialog to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="e74a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e74a3-105">Syntax</span></span>


```JScript
IShellDispatch.FileRun()
```


```VB

IShellDispatch.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="e74a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e74a3-106">Parameters</span></span>

<span data-ttu-id="e74a3-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e74a3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e74a3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e74a3-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e74a3-109">JScript</span><span class="sxs-lookup"><span data-stu-id="e74a3-109">JScript</span></span>

<span data-ttu-id="e74a3-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e74a3-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="e74a3-111">VB</span><span class="sxs-lookup"><span data-stu-id="e74a3-111">VB</span></span>

<span data-ttu-id="e74a3-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e74a3-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e74a3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e74a3-113">Remarks</span></span>

<span data-ttu-id="e74a3-114">Esse método é implementado e acessado por meio do método [**shell. FileRun**](shell-filerun.md) .</span><span class="sxs-lookup"><span data-stu-id="e74a3-114">This method is implemented and accessed through the [**Shell.FileRun**](shell-filerun.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="e74a3-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e74a3-115">Examples</span></span>

<span data-ttu-id="e74a3-116">Os exemplos a seguir mostram o uso de **FileRun** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e74a3-116">The following examples show the use of **FileRun** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e74a3-117">JScript</span><span class="sxs-lookup"><span data-stu-id="e74a3-117">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FileRun();
    }
</script>
```



<span data-ttu-id="e74a3-118">VBScript</span><span class="sxs-lookup"><span data-stu-id="e74a3-118">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e74a3-119">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e74a3-119">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e74a3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e74a3-120">Requirements</span></span>



| <span data-ttu-id="e74a3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e74a3-121">Requirement</span></span> | <span data-ttu-id="e74a3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e74a3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e74a3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e74a3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e74a3-124">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e74a3-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e74a3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e74a3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e74a3-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e74a3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e74a3-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e74a3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e74a3-128"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e74a3-128"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e74a3-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="e74a3-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e74a3-130"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e74a3-130"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e74a3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e74a3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e74a3-132"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e74a3-132"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




