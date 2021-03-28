---
description: Atualiza o conteúdo do menu iniciar. Usado apenas com sistemas anteriores ao Windows XP.
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
ms.openlocfilehash: a5812312c846026f4e0c7d2a4f6a5f857a572a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967954"
---
# <a name="shellrefreshmenu-method"></a><span data-ttu-id="b5eba-104">Método Shell. RefreshMenu</span><span class="sxs-lookup"><span data-stu-id="b5eba-104">Shell.RefreshMenu method</span></span>

<span data-ttu-id="b5eba-105">Atualiza o conteúdo do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="b5eba-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="b5eba-106">Usado apenas com sistemas anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b5eba-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5eba-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5eba-107">Syntax</span></span>


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a><span data-ttu-id="b5eba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5eba-108">Parameters</span></span>

<span data-ttu-id="b5eba-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b5eba-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5eba-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5eba-110">Remarks</span></span>

<span data-ttu-id="b5eba-111">A funcionalidade que o **RefreshMenu** fornece é tratada automaticamente no Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b5eba-111">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="b5eba-112">Não chame esse método nesse sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b5eba-112">Do not call this method under that operating system.</span></span>

## <a name="examples"></a><span data-ttu-id="b5eba-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5eba-113">Examples</span></span>

<span data-ttu-id="b5eba-114">O exemplo a seguir mostra **RefreshMenu** em uso.</span><span class="sxs-lookup"><span data-stu-id="b5eba-114">The following example shows **RefreshMenu** in use.</span></span> <span data-ttu-id="b5eba-115">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b5eba-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b5eba-116">JScript</span><span class="sxs-lookup"><span data-stu-id="b5eba-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="b5eba-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="b5eba-117">VBScript:</span></span>


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



<span data-ttu-id="b5eba-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b5eba-118">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b5eba-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5eba-119">Requirements</span></span>



| <span data-ttu-id="b5eba-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5eba-120">Requirement</span></span> | <span data-ttu-id="b5eba-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b5eba-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5eba-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5eba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b5eba-123">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b5eba-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b5eba-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5eba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b5eba-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b5eba-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b5eba-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b5eba-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5eba-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5eba-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b5eba-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="b5eba-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5eba-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5eba-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b5eba-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b5eba-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5eba-131"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b5eba-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




