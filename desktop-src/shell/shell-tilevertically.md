---
description: Organiza todas as janelas na área de trabalho verticalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar janelas de peças verticalmente.
ms.assetid: 7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea
title: Método Shell. TileVertically (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8ecea9df2bcbb2e410841231ed7eca170872e015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968164"
---
# <a name="shelltilevertically-method"></a><span data-ttu-id="b7822-104">Método Shell. TileVertically</span><span class="sxs-lookup"><span data-stu-id="b7822-104">Shell.TileVertically method</span></span>

<span data-ttu-id="b7822-105">Organiza todas as janelas na área de trabalho verticalmente.</span><span class="sxs-lookup"><span data-stu-id="b7822-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="b7822-106">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **janelas de peças verticalmente**.</span><span class="sxs-lookup"><span data-stu-id="b7822-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Vertically**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7822-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7822-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileVertically()
```


```VB

Shell.TileVertically() As Integer
```





## <a name="parameters"></a><span data-ttu-id="b7822-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7822-108">Parameters</span></span>

<span data-ttu-id="b7822-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b7822-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="b7822-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b7822-110">Examples</span></span>

<span data-ttu-id="b7822-111">O exemplo a seguir mostra **TileVertically** em uso.</span><span class="sxs-lookup"><span data-stu-id="b7822-111">The following example shows **TileVertically** in use.</span></span> <span data-ttu-id="b7822-112">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b7822-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b7822-113">JScript</span><span class="sxs-lookup"><span data-stu-id="b7822-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileVertically();
    }
</script>
```



<span data-ttu-id="b7822-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="b7822-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b7822-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b7822-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b7822-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7822-116">Requirements</span></span>



| <span data-ttu-id="b7822-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7822-117">Requirement</span></span> | <span data-ttu-id="b7822-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b7822-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7822-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7822-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b7822-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b7822-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b7822-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7822-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b7822-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b7822-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b7822-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b7822-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7822-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7822-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b7822-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="b7822-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7822-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7822-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b7822-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b7822-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7822-128"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b7822-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




