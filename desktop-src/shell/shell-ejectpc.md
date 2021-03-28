---
description: Ejeta o computador de sua estação de encaixe. Isso é o mesmo que clicar no menu iniciar e selecionar Ejetar PC se o seu computador oferecer suporte a esse comando.
ms.assetid: eaba3dce-8fea-453f-90c2-4a9b5cb05ecc
title: Método Shell. EjectPC (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 355d75b2ffaca9c9f90e66fbc535333a84bfa45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967989"
---
# <a name="shellejectpc-method"></a><span data-ttu-id="f6dff-104">Método Shell. EjectPC</span><span class="sxs-lookup"><span data-stu-id="f6dff-104">Shell.EjectPC method</span></span>

<span data-ttu-id="f6dff-105">Ejeta o computador de sua estação de encaixe.</span><span class="sxs-lookup"><span data-stu-id="f6dff-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="f6dff-106">Isso é o mesmo que clicar no menu **Iniciar** e selecionar **Ejetar PC** se o seu computador oferecer suporte a esse comando.</span><span class="sxs-lookup"><span data-stu-id="f6dff-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6dff-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6dff-107">Syntax</span></span>


```JScript
Shell.EjectPC()
```


```VB

Shell.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="f6dff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6dff-108">Parameters</span></span>

<span data-ttu-id="f6dff-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f6dff-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6dff-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6dff-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f6dff-111">JScript</span><span class="sxs-lookup"><span data-stu-id="f6dff-111">JScript</span></span>

<span data-ttu-id="f6dff-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f6dff-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f6dff-113">VB</span><span class="sxs-lookup"><span data-stu-id="f6dff-113">VB</span></span>

<span data-ttu-id="f6dff-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f6dff-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="f6dff-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6dff-115">Examples</span></span>

<span data-ttu-id="f6dff-116">O exemplo a seguir mostra **EjectPC** em uso.</span><span class="sxs-lookup"><span data-stu-id="f6dff-116">The following example shows **EjectPC** in use.</span></span> <span data-ttu-id="f6dff-117">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f6dff-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f6dff-118">JScript</span><span class="sxs-lookup"><span data-stu-id="f6dff-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.EjectPC();
    }
</script>
```



<span data-ttu-id="f6dff-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="f6dff-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f6dff-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f6dff-120">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f6dff-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6dff-121">Requirements</span></span>



| <span data-ttu-id="f6dff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6dff-122">Requirement</span></span> | <span data-ttu-id="f6dff-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f6dff-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6dff-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6dff-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f6dff-125">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f6dff-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f6dff-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6dff-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f6dff-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6dff-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f6dff-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f6dff-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6dff-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6dff-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f6dff-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="f6dff-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6dff-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6dff-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f6dff-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f6dff-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6dff-133"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f6dff-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




