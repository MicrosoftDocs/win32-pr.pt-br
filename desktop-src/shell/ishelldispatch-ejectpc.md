---
description: Ejeta o computador de sua estação de encaixe. Isso é o mesmo que clicar no menu iniciar e selecionar Ejetar PC se o seu computador oferecer suporte a esse comando.
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
title: Método IShellDispatch. EjectPC (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d85dd8c007338dca3d68183bc9ba3fbd333195ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164751"
---
# <a name="ishelldispatchejectpc-method"></a><span data-ttu-id="59a68-104">Método IShellDispatch. EjectPC</span><span class="sxs-lookup"><span data-stu-id="59a68-104">IShellDispatch.EjectPC method</span></span>

<span data-ttu-id="59a68-105">Ejeta o computador de sua estação de encaixe.</span><span class="sxs-lookup"><span data-stu-id="59a68-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="59a68-106">Isso é o mesmo que clicar no menu **Iniciar** e selecionar **Ejetar PC** se o seu computador oferecer suporte a esse comando.</span><span class="sxs-lookup"><span data-stu-id="59a68-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a68-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59a68-107">Syntax</span></span>


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="59a68-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59a68-108">Parameters</span></span>

<span data-ttu-id="59a68-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="59a68-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59a68-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59a68-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="59a68-111">JScript</span><span class="sxs-lookup"><span data-stu-id="59a68-111">JScript</span></span>

<span data-ttu-id="59a68-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="59a68-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="59a68-113">VB</span><span class="sxs-lookup"><span data-stu-id="59a68-113">VB</span></span>

<span data-ttu-id="59a68-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="59a68-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59a68-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="59a68-115">Remarks</span></span>

<span data-ttu-id="59a68-116">Esse método é implementado e acessado por meio do método [**shell. EjectPC**](shell-ejectpc.md) .</span><span class="sxs-lookup"><span data-stu-id="59a68-116">This method is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="59a68-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="59a68-117">Examples</span></span>

<span data-ttu-id="59a68-118">Os exemplos a seguir mostram o uso de **EjectPC** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="59a68-118">The following examples show the use of **EjectPC** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="59a68-119">JScript</span><span class="sxs-lookup"><span data-stu-id="59a68-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



<span data-ttu-id="59a68-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="59a68-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="59a68-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="59a68-121">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="59a68-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59a68-122">Requirements</span></span>



| <span data-ttu-id="59a68-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="59a68-123">Requirement</span></span> | <span data-ttu-id="59a68-124">Valor</span><span class="sxs-lookup"><span data-stu-id="59a68-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59a68-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59a68-125">Minimum supported client</span></span><br/> | <span data-ttu-id="59a68-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="59a68-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="59a68-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59a68-127">Minimum supported server</span></span><br/> | <span data-ttu-id="59a68-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="59a68-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="59a68-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="59a68-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="59a68-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="59a68-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="59a68-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="59a68-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="59a68-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="59a68-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="59a68-133">DLL</span><span class="sxs-lookup"><span data-stu-id="59a68-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59a68-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="59a68-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




