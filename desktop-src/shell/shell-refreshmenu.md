---
description: Saiba mais sobre o método Shell. RefreshMenu, que atualiza o conteúdo do menu iniciar. Usado apenas com sistemas anteriores ao Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Método Shell. RefreshMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 90020cd128f5cbc585bd7bc9ab33a8a81c745f8e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404529"
---
# <a name="shellrefreshmenu-method"></a><span data-ttu-id="bed27-104">Método Shell. RefreshMenu</span><span class="sxs-lookup"><span data-stu-id="bed27-104">Shell.RefreshMenu method</span></span>

<span data-ttu-id="bed27-105">Atualiza o conteúdo do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="bed27-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="bed27-106">Usado apenas com sistemas anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bed27-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="bed27-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bed27-107">Syntax</span></span>


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a><span data-ttu-id="bed27-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bed27-108">Parameters</span></span>

<span data-ttu-id="bed27-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bed27-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bed27-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="bed27-110">Remarks</span></span>

<span data-ttu-id="bed27-111">A funcionalidade que o **RefreshMenu** fornece é tratada automaticamente no Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="bed27-111">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="bed27-112">Não chame esse método nesse sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bed27-112">Do not call this method under that operating system.</span></span>

## <a name="examples"></a><span data-ttu-id="bed27-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bed27-113">Examples</span></span>

<span data-ttu-id="bed27-114">O exemplo a seguir mostra **RefreshMenu** em uso.</span><span class="sxs-lookup"><span data-stu-id="bed27-114">The following example shows **RefreshMenu** in use.</span></span> <span data-ttu-id="bed27-115">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bed27-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bed27-116">JScript</span><span class="sxs-lookup"><span data-stu-id="bed27-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="bed27-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="bed27-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="bed27-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="bed27-118">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bed27-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bed27-119">Requirements</span></span>



| <span data-ttu-id="bed27-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bed27-120">Requirement</span></span> | <span data-ttu-id="bed27-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bed27-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bed27-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bed27-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bed27-123">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bed27-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bed27-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bed27-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bed27-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bed27-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bed27-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bed27-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bed27-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bed27-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bed27-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="bed27-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bed27-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bed27-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bed27-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bed27-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bed27-131"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="bed27-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




