---
description: Organiza todas as janelas na área de trabalho verticalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar Mostrar janelas lado a lado.
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
title: Método IShellDispatch. TileVertically (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 42f98ae99814495029c67d41b05e86182c6b8b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967532"
---
# <a name="ishelldispatchtilevertically-method"></a><span data-ttu-id="9ff7d-104">Método IShellDispatch. TileVertically</span><span class="sxs-lookup"><span data-stu-id="9ff7d-104">IShellDispatch.TileVertically method</span></span>

<span data-ttu-id="9ff7d-105">Organiza todas as janelas na área de trabalho verticalmente.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="9ff7d-106">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **Mostrar janelas lado a lado**.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows side by side**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff7d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ff7d-107">Syntax</span></span>


```JScript
IShellDispatch.TileVertically()
```


```VB

IShellDispatch.TileVertically()
```





## <a name="parameters"></a><span data-ttu-id="9ff7d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ff7d-108">Parameters</span></span>

<span data-ttu-id="9ff7d-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ff7d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ff7d-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9ff7d-111">JScript</span><span class="sxs-lookup"><span data-stu-id="9ff7d-111">JScript</span></span>

<span data-ttu-id="9ff7d-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="9ff7d-113">VB</span><span class="sxs-lookup"><span data-stu-id="9ff7d-113">VB</span></span>

<span data-ttu-id="9ff7d-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff7d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ff7d-115">Remarks</span></span>

<span data-ttu-id="9ff7d-116">Esse método é implementado e acessado por meio do método [**shell. TileVertically**](shell-tilevertically.md) .</span><span class="sxs-lookup"><span data-stu-id="9ff7d-116">This method is implemented and accessed through the [**Shell.TileVertically**](shell-tilevertically.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="9ff7d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ff7d-117">Examples</span></span>

<span data-ttu-id="9ff7d-118">Os exemplos a seguir mostram o uso de **TileVertically** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9ff7d-118">The following examples show the use of **TileVertically** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9ff7d-119">JScript</span><span class="sxs-lookup"><span data-stu-id="9ff7d-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
    }
</script>
```



<span data-ttu-id="9ff7d-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="9ff7d-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9ff7d-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="9ff7d-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9ff7d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ff7d-122">Requirements</span></span>



| <span data-ttu-id="9ff7d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ff7d-123">Requirement</span></span> | <span data-ttu-id="9ff7d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9ff7d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff7d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ff7d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff7d-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9ff7d-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9ff7d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ff7d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff7d-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9ff7d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9ff7d-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9ff7d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff7d-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ff7d-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9ff7d-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="9ff7d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9ff7d-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9ff7d-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9ff7d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9ff7d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ff7d-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9ff7d-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




