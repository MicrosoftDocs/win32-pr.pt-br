---
description: Atualiza o conteúdo do menu iniciar. Usado apenas com sistemas anteriores ao Windows XP.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Método IShellDispatch. RefreshMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 98728ef48ffb9ef4383cf9ba567606758b7a015c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967536"
---
# <a name="ishelldispatchrefreshmenu-method"></a><span data-ttu-id="b3cd8-104">Método IShellDispatch. RefreshMenu</span><span class="sxs-lookup"><span data-stu-id="b3cd8-104">IShellDispatch.RefreshMenu method</span></span>

<span data-ttu-id="b3cd8-105">Atualiza o conteúdo do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="b3cd8-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="b3cd8-106">Usado apenas com sistemas anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b3cd8-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3cd8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3cd8-107">Syntax</span></span>


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a><span data-ttu-id="b3cd8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3cd8-108">Parameters</span></span>

<span data-ttu-id="b3cd8-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b3cd8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3cd8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3cd8-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b3cd8-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b3cd8-111">JScript</span></span>

<span data-ttu-id="b3cd8-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b3cd8-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b3cd8-113">VB</span><span class="sxs-lookup"><span data-stu-id="b3cd8-113">VB</span></span>

<span data-ttu-id="b3cd8-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b3cd8-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3cd8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3cd8-115">Remarks</span></span>

<span data-ttu-id="b3cd8-116">Esse método é implementado e acessado por meio do método [**shell. trayproperties**](shell-trayproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="b3cd8-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

<span data-ttu-id="b3cd8-117">A funcionalidade que o **RefreshMenu** fornece é tratada automaticamente no Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b3cd8-117">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="b3cd8-118">Não chame esse método no Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b3cd8-118">Do not call this method on Windows XP or later.</span></span>

## <a name="examples"></a><span data-ttu-id="b3cd8-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b3cd8-119">Examples</span></span>

<span data-ttu-id="b3cd8-120">Os exemplos a seguir mostram o uso de **RefreshMenu** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b3cd8-120">The following examples show the use of **RefreshMenu** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b3cd8-121">JScript</span><span class="sxs-lookup"><span data-stu-id="b3cd8-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="b3cd8-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="b3cd8-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b3cd8-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b3cd8-123">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b3cd8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3cd8-124">Requirements</span></span>



| <span data-ttu-id="b3cd8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3cd8-125">Requirement</span></span> | <span data-ttu-id="b3cd8-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b3cd8-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3cd8-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3cd8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b3cd8-128">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b3cd8-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b3cd8-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3cd8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b3cd8-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3cd8-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b3cd8-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b3cd8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3cd8-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3cd8-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b3cd8-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="b3cd8-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3cd8-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3cd8-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b3cd8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b3cd8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3cd8-136"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b3cd8-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




