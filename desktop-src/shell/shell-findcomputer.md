---
description: 'Exibe a caixa de diálogo resultados da pesquisa: computadores. A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.'
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360
title: Método Shell. FindComputer (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3824eeb98bfac11e007d1bf7dd9f89153a7b73ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968173"
---
# <a name="shellfindcomputer-method"></a><span data-ttu-id="070fe-104">Método Shell. FindComputer</span><span class="sxs-lookup"><span data-stu-id="070fe-104">Shell.FindComputer method</span></span>

<span data-ttu-id="070fe-105">Exibe a caixa de diálogo **resultados da pesquisa: computadores** .</span><span class="sxs-lookup"><span data-stu-id="070fe-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="070fe-106">A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="070fe-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="070fe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="070fe-107">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="070fe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="070fe-108">Parameters</span></span>

<span data-ttu-id="070fe-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="070fe-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="070fe-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="070fe-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="070fe-111">JScript</span><span class="sxs-lookup"><span data-stu-id="070fe-111">JScript</span></span>

<span data-ttu-id="070fe-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="070fe-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="070fe-113">VB</span><span class="sxs-lookup"><span data-stu-id="070fe-113">VB</span></span>

<span data-ttu-id="070fe-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="070fe-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="070fe-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="070fe-115">Examples</span></span>

<span data-ttu-id="070fe-116">O exemplo a seguir mostra **FindComputer** em uso.</span><span class="sxs-lookup"><span data-stu-id="070fe-116">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="070fe-117">O resultado desse código é o mesmo que pressionar o botão **Iniciar** , clicar em **Pesquisar**, clicar na opção **impressoras, computadores ou pessoas** e clicar em **um computador na rede**.</span><span class="sxs-lookup"><span data-stu-id="070fe-117">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="070fe-118">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="070fe-118">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="070fe-119">JScript</span><span class="sxs-lookup"><span data-stu-id="070fe-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="070fe-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="070fe-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="070fe-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="070fe-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="070fe-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="070fe-122">Requirements</span></span>



| <span data-ttu-id="070fe-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="070fe-123">Requirement</span></span> | <span data-ttu-id="070fe-124">Valor</span><span class="sxs-lookup"><span data-stu-id="070fe-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="070fe-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="070fe-125">Minimum supported client</span></span><br/> | <span data-ttu-id="070fe-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="070fe-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="070fe-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="070fe-127">Minimum supported server</span></span><br/> | <span data-ttu-id="070fe-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="070fe-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="070fe-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="070fe-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="070fe-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="070fe-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="070fe-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="070fe-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="070fe-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="070fe-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="070fe-133">DLL</span><span class="sxs-lookup"><span data-stu-id="070fe-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="070fe-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="070fe-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




