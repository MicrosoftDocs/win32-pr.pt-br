---
description: 'Exibe a caixa de diálogo localizar: todos os arquivos. Isso é o mesmo que clicar no menu iniciar e Selecionar Pesquisar (ou seu equivalente em sistemas anteriores ao Windows XP).'
ms.assetid: cccdd3ea-b52a-4fbe-b4c5-1efc1dd6d770
title: Método Shell. FindFiles (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f3e6551dc41fd8d6a040ada8000f0b46e81a5dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171187"
---
# <a name="shellfindfiles-method"></a><span data-ttu-id="839e3-104">Método Shell. FindFiles</span><span class="sxs-lookup"><span data-stu-id="839e3-104">Shell.FindFiles method</span></span>

<span data-ttu-id="839e3-105">Exibe a caixa de diálogo **localizar: todos os arquivos** .</span><span class="sxs-lookup"><span data-stu-id="839e3-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="839e3-106">Isso é o mesmo que clicar no menu **Iniciar** e selecionar **Pesquisar** (ou seu equivalente em sistemas anteriores ao Windows XP).</span><span class="sxs-lookup"><span data-stu-id="839e3-106">This is the same as clicking the **Start** menu and then selecting **Search** (or its equivalent under systems earlier than Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="839e3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="839e3-107">Syntax</span></span>


```JScript
Shell.FindFiles()
```


```VB

Shell.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="839e3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="839e3-108">Parameters</span></span>

<span data-ttu-id="839e3-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="839e3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="839e3-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="839e3-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="839e3-111">JScript</span><span class="sxs-lookup"><span data-stu-id="839e3-111">JScript</span></span>

<span data-ttu-id="839e3-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="839e3-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="839e3-113">VB</span><span class="sxs-lookup"><span data-stu-id="839e3-113">VB</span></span>

<span data-ttu-id="839e3-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="839e3-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="839e3-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="839e3-115">Examples</span></span>

<span data-ttu-id="839e3-116">O exemplo a seguir mostra **FindFiles** em uso.</span><span class="sxs-lookup"><span data-stu-id="839e3-116">The following example shows **FindFiles** in use.</span></span> <span data-ttu-id="839e3-117">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="839e3-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="839e3-118">JScript</span><span class="sxs-lookup"><span data-stu-id="839e3-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Shell_FindFiles();
    }
</script>
```



<span data-ttu-id="839e3-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="839e3-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindFilesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FindFiles

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="839e3-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="839e3-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="839e3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="839e3-121">Requirements</span></span>



| <span data-ttu-id="839e3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="839e3-122">Requirement</span></span> | <span data-ttu-id="839e3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="839e3-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="839e3-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="839e3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="839e3-125">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="839e3-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="839e3-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="839e3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="839e3-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="839e3-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="839e3-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="839e3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="839e3-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="839e3-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="839e3-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="839e3-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="839e3-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="839e3-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="839e3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="839e3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="839e3-133"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="839e3-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




