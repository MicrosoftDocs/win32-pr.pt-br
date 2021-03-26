---
description: Exibe a caixa de diálogo Data e hora. Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar ajustar data/hora.
ms.assetid: D4B949F6-5508-4624-9706-491184703DC6
title: Método IShellDispatch. setTime (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c9e687ea89cad4715aeacf72a2a33792fba9f7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827401"
---
# <a name="ishelldispatchsettime-method"></a><span data-ttu-id="cee40-104">Método IShellDispatch. setTime</span><span class="sxs-lookup"><span data-stu-id="cee40-104">IShellDispatch.SetTime method</span></span>

<span data-ttu-id="cee40-105">Exibe a caixa de diálogo **data e hora** .</span><span class="sxs-lookup"><span data-stu-id="cee40-105">Displays the **Date and Time** dialog box.</span></span> <span data-ttu-id="cee40-106">Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar **Ajustar data/hora**.</span><span class="sxs-lookup"><span data-stu-id="cee40-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust date/time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cee40-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cee40-107">Syntax</span></span>


```JScript
IShellDispatch.SetTime()
```


```VB

IShellDispatch.SetTime()
```





## <a name="parameters"></a><span data-ttu-id="cee40-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cee40-108">Parameters</span></span>

<span data-ttu-id="cee40-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cee40-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cee40-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cee40-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cee40-111">JScript</span><span class="sxs-lookup"><span data-stu-id="cee40-111">JScript</span></span>

<span data-ttu-id="cee40-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cee40-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="cee40-113">VB</span><span class="sxs-lookup"><span data-stu-id="cee40-113">VB</span></span>

<span data-ttu-id="cee40-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cee40-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cee40-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cee40-115">Remarks</span></span>

<span data-ttu-id="cee40-116">Esse método é implementado e acessado por meio do método [**shell. setTime**](shell-settime.md) .</span><span class="sxs-lookup"><span data-stu-id="cee40-116">This method is implemented and accessed through the [**Shell.SetTime**](shell-settime.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="cee40-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cee40-117">Examples</span></span>

<span data-ttu-id="cee40-118">Os exemplos a seguir mostram o uso de **setTime** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cee40-118">The following examples show the use of **SetTime** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cee40-119">JScript</span><span class="sxs-lookup"><span data-stu-id="cee40-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.SetTime();
    }
</script>
```



<span data-ttu-id="cee40-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="cee40-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.SetTime
 
        set objShell = nothing
    end function
```



<span data-ttu-id="cee40-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cee40-121">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.SetTime
 
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="cee40-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cee40-122">Requirements</span></span>



| <span data-ttu-id="cee40-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cee40-123">Requirement</span></span> | <span data-ttu-id="cee40-124">Valor</span><span class="sxs-lookup"><span data-stu-id="cee40-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee40-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cee40-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cee40-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cee40-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cee40-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cee40-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cee40-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cee40-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cee40-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cee40-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cee40-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cee40-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cee40-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="cee40-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cee40-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cee40-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cee40-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cee40-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cee40-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="cee40-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




