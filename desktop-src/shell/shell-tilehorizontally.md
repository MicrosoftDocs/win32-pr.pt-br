---
description: Organiza todas as janelas na área de trabalho horizontalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar janelas de bloco horizontalmente.
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: Método Shell. TileHorizontally (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e295d0a7847afc0cb405f3ab9141e54ae424e9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170084"
---
# <a name="shelltilehorizontally-method"></a><span data-ttu-id="99622-104">Método Shell. TileHorizontally</span><span class="sxs-lookup"><span data-stu-id="99622-104">Shell.TileHorizontally method</span></span>

<span data-ttu-id="99622-105">Organiza todas as janelas na área de trabalho horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="99622-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="99622-106">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **janelas de bloco horizontalmente**.</span><span class="sxs-lookup"><span data-stu-id="99622-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Horizontally**.</span></span>

## <a name="syntax"></a><span data-ttu-id="99622-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99622-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a><span data-ttu-id="99622-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99622-108">Parameters</span></span>

<span data-ttu-id="99622-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="99622-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="99622-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="99622-110">Examples</span></span>

<span data-ttu-id="99622-111">O exemplo a seguir mostra **TileHorizontally** em uso.</span><span class="sxs-lookup"><span data-stu-id="99622-111">The following example shows **TileHorizontally** in use.</span></span> <span data-ttu-id="99622-112">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="99622-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="99622-113">JScript</span><span class="sxs-lookup"><span data-stu-id="99622-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="99622-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="99622-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="99622-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="99622-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="99622-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99622-116">Requirements</span></span>



| <span data-ttu-id="99622-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="99622-117">Requirement</span></span> | <span data-ttu-id="99622-118">Valor</span><span class="sxs-lookup"><span data-stu-id="99622-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99622-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99622-119">Minimum supported client</span></span><br/> | <span data-ttu-id="99622-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="99622-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="99622-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99622-121">Minimum supported server</span></span><br/> | <span data-ttu-id="99622-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99622-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="99622-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99622-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="99622-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="99622-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="99622-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="99622-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99622-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="99622-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="99622-127">DLL</span><span class="sxs-lookup"><span data-stu-id="99622-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99622-128"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="99622-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




