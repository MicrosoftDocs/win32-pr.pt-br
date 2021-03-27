---
description: 'Exibe a caixa de diálogo resultados da pesquisa: computadores. A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.'
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257
title: Método IShellDispatch. FindComputer (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ad928b6860a85126a714a08f3bc3df9d4aff67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967540"
---
# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="92a76-104">Método IShellDispatch. FindComputer</span><span class="sxs-lookup"><span data-stu-id="92a76-104">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="92a76-105">Exibe a caixa de diálogo **resultados da pesquisa: computadores** .</span><span class="sxs-lookup"><span data-stu-id="92a76-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="92a76-106">A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="92a76-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a76-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92a76-107">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="92a76-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92a76-108">Parameters</span></span>

<span data-ttu-id="92a76-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="92a76-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92a76-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92a76-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="92a76-111">JScript</span><span class="sxs-lookup"><span data-stu-id="92a76-111">JScript</span></span>

<span data-ttu-id="92a76-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="92a76-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="92a76-113">VB</span><span class="sxs-lookup"><span data-stu-id="92a76-113">VB</span></span>

<span data-ttu-id="92a76-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="92a76-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a76-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="92a76-115">Remarks</span></span>

<span data-ttu-id="92a76-116">Esse método é implementado e acessado por meio do método [**shell. FindComputer**](shell-findcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="92a76-116">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="92a76-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="92a76-117">Examples</span></span>

<span data-ttu-id="92a76-118">Os exemplos a seguir mostram o uso de **FindComputer** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="92a76-118">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="92a76-119">JScript</span><span class="sxs-lookup"><span data-stu-id="92a76-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="92a76-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="92a76-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="92a76-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="92a76-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="92a76-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92a76-122">Requirements</span></span>



| <span data-ttu-id="92a76-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="92a76-123">Requirement</span></span> | <span data-ttu-id="92a76-124">Valor</span><span class="sxs-lookup"><span data-stu-id="92a76-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a76-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92a76-125">Minimum supported client</span></span><br/> | <span data-ttu-id="92a76-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="92a76-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="92a76-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92a76-127">Minimum supported server</span></span><br/> | <span data-ttu-id="92a76-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="92a76-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="92a76-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="92a76-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="92a76-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="92a76-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="92a76-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="92a76-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="92a76-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="92a76-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="92a76-133">DLL</span><span class="sxs-lookup"><span data-stu-id="92a76-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92a76-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="92a76-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




