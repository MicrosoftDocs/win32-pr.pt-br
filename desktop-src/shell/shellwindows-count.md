---
description: Contém o número de itens na coleção.
ms.assetid: 0113cc32-2197-4004-99a1-89fe10828e5f
title: Propriedade ShellWindows. Count (textdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a8d5b9e605650ba7d3cb6036e8abfac58c0b8597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968191"
---
# <a name="shellwindowscount-property"></a><span data-ttu-id="b1ce6-103">Propriedade ShellWindows. Count</span><span class="sxs-lookup"><span data-stu-id="b1ce6-103">ShellWindows.Count property</span></span>

<span data-ttu-id="b1ce6-104">Contém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="b1ce6-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="b1ce6-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b1ce6-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ce6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1ce6-106">Syntax</span></span>


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a><span data-ttu-id="b1ce6-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b1ce6-107">Property value</span></span>

<span data-ttu-id="b1ce6-108">Um **inteiro** que contém um valor para a propriedade **Count** .</span><span class="sxs-lookup"><span data-stu-id="b1ce6-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="b1ce6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b1ce6-109">Examples</span></span>

<span data-ttu-id="b1ce6-110">O exemplo a seguir mostra a **contagem** em uso.</span><span class="sxs-lookup"><span data-stu-id="b1ce6-110">The following example shows **Count** in use.</span></span> <span data-ttu-id="b1ce6-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b1ce6-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b1ce6-112">JScript</span><span class="sxs-lookup"><span data-stu-id="b1ce6-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Shell_Windows();
        if (objShellWindows != null)
        {
            var nCount;
            
            nCount = objShellWindows.Count;
            alert(nCount);
        }
    }
</script>
```



<span data-ttu-id="b1ce6-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="b1ce6-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsCountVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim nCount
            nCount = objShellWindows.Count

            alert(nCount)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b1ce6-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b1ce6-114">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsCountVB()
    Dim objShell         As Shell
    Dim objShellWindows  As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b1ce6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1ce6-115">Requirements</span></span>



| <span data-ttu-id="b1ce6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1ce6-116">Requirement</span></span> | <span data-ttu-id="b1ce6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b1ce6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ce6-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1ce6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ce6-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b1ce6-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b1ce6-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1ce6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1ce6-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b1ce6-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b1ce6-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b1ce6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1ce6-123"><dt>O textdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1ce6-123"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="b1ce6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b1ce6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1ce6-125"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b1ce6-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




