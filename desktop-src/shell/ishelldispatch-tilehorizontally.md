---
description: Organiza todas as janelas na área de trabalho horizontalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar Mostrar janelas empilhadas.
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
title: Método IShellDispatch. TileHorizontally (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 06491f797de4a9fcb5c431d85cff71fbc78d605c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090842"
---
# <a name="ishelldispatchtilehorizontally-method"></a><span data-ttu-id="0274f-104">Método IShellDispatch. TileHorizontally</span><span class="sxs-lookup"><span data-stu-id="0274f-104">IShellDispatch.TileHorizontally method</span></span>

<span data-ttu-id="0274f-105">Organiza todas as janelas na área de trabalho horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="0274f-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="0274f-106">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **Mostrar janelas empilhadas**.</span><span class="sxs-lookup"><span data-stu-id="0274f-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows stacked**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0274f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0274f-107">Syntax</span></span>


```JScript
IShellDispatch.TileHorizontally()
```


```VB

IShellDispatch.TileHorizontally()
```





## <a name="parameters"></a><span data-ttu-id="0274f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0274f-108">Parameters</span></span>

<span data-ttu-id="0274f-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0274f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0274f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0274f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0274f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="0274f-111">JScript</span></span>

<span data-ttu-id="0274f-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0274f-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="0274f-113">VB</span><span class="sxs-lookup"><span data-stu-id="0274f-113">VB</span></span>

<span data-ttu-id="0274f-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0274f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0274f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0274f-115">Remarks</span></span>

<span data-ttu-id="0274f-116">Esse método é implementado e acessado por meio do método [**shell. TileHorizontally**](shell-tilehorizontally.md) .</span><span class="sxs-lookup"><span data-stu-id="0274f-116">This method is implemented and accessed through the [**Shell.TileHorizontally**](shell-tilehorizontally.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="0274f-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0274f-117">Examples</span></span>

<span data-ttu-id="0274f-118">O exemplo a seguir mostra o uso de **TileHorizontally** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0274f-118">The following example shows the use of **TileHorizontally** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0274f-119">JScript</span><span class="sxs-lookup"><span data-stu-id="0274f-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="0274f-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="0274f-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="0274f-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="0274f-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0274f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0274f-122">Requirements</span></span>



| <span data-ttu-id="0274f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0274f-123">Requirement</span></span> | <span data-ttu-id="0274f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0274f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0274f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0274f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0274f-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0274f-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0274f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0274f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0274f-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0274f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0274f-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0274f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0274f-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0274f-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0274f-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="0274f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0274f-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0274f-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0274f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0274f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0274f-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="0274f-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




