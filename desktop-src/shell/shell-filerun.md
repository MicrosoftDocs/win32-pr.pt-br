---
description: Exibe a caixa de diálogo Executar para o usuário. Esse método tem o mesmo efeito que clicar no menu iniciar e selecionar executar.
ms.assetid: bb984777-e09f-41e6-8359-51c5291654f7
title: Método Shell. FileRun (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ebccf11ea21fdd4ceba2563a6110c1eb2494947b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968176"
---
# <a name="shellfilerun-method"></a><span data-ttu-id="3200a-104">Método Shell. FileRun</span><span class="sxs-lookup"><span data-stu-id="3200a-104">Shell.FileRun method</span></span>

<span data-ttu-id="3200a-105">Exibe a caixa de diálogo **executar** para o usuário.</span><span class="sxs-lookup"><span data-stu-id="3200a-105">Displays the **Run** dialog to the user.</span></span> <span data-ttu-id="3200a-106">Esse método tem o mesmo efeito que clicar no menu **Iniciar** e selecionar **executar**.</span><span class="sxs-lookup"><span data-stu-id="3200a-106">This method has the same effect as clicking the **Start** menu and selecting **Run**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3200a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3200a-107">Syntax</span></span>


```JScript
Shell.FileRun()
```


```VB

Shell.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="3200a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3200a-108">Parameters</span></span>

<span data-ttu-id="3200a-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3200a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3200a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3200a-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="3200a-111">JScript</span><span class="sxs-lookup"><span data-stu-id="3200a-111">JScript</span></span>

<span data-ttu-id="3200a-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3200a-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="3200a-113">VB</span><span class="sxs-lookup"><span data-stu-id="3200a-113">VB</span></span>

<span data-ttu-id="3200a-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3200a-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="3200a-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3200a-115">Examples</span></span>

<span data-ttu-id="3200a-116">O exemplo a seguir mostra **FileRun** em uso.</span><span class="sxs-lookup"><span data-stu-id="3200a-116">The following example shows **FileRun** in use.</span></span> <span data-ttu-id="3200a-117">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3200a-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3200a-118">JScript</span><span class="sxs-lookup"><span data-stu-id="3200a-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FileRun();
    }
</script>
```



<span data-ttu-id="3200a-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="3200a-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="3200a-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3200a-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3200a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3200a-121">Requirements</span></span>



| <span data-ttu-id="3200a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3200a-122">Requirement</span></span> | <span data-ttu-id="3200a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3200a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3200a-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3200a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3200a-125">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3200a-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3200a-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3200a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3200a-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3200a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3200a-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3200a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3200a-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3200a-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3200a-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="3200a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3200a-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3200a-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3200a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3200a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3200a-133"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3200a-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




