---
description: Método Shell. Trayproperties – exibe a barra de tarefas e a caixa de diálogo Propriedades do menu iniciar. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar Propriedades.
ms.assetid: 0d82d847-9e6f-461e-b938-fe8fd49a636f
title: Método Shell. Trayproperties (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e09f6833fbf07c99fdbce9c02b020bcbb5361408
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104094"
---
# <a name="shelltrayproperties-method"></a><span data-ttu-id="8e6b7-104">Método Shell. Trayproperties</span><span class="sxs-lookup"><span data-stu-id="8e6b7-104">Shell.TrayProperties method</span></span>

<span data-ttu-id="8e6b7-105">Exibe a **barra de tarefas e a caixa de diálogo Propriedades do menu iniciar** .</span><span class="sxs-lookup"><span data-stu-id="8e6b7-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="8e6b7-106">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="8e6b7-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e6b7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e6b7-107">Syntax</span></span>


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a><span data-ttu-id="8e6b7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e6b7-108">Parameters</span></span>

<span data-ttu-id="8e6b7-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8e6b7-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="8e6b7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e6b7-110">Examples</span></span>

<span data-ttu-id="8e6b7-111">O exemplo a seguir mostra **trayproperties** em uso.</span><span class="sxs-lookup"><span data-stu-id="8e6b7-111">The following example shows **TrayProperties** in use.</span></span> <span data-ttu-id="8e6b7-112">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8e6b7-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8e6b7-113">JScript</span><span class="sxs-lookup"><span data-stu-id="8e6b7-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



<span data-ttu-id="8e6b7-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="8e6b7-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="8e6b7-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8e6b7-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8e6b7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e6b7-116">Requirements</span></span>



| <span data-ttu-id="8e6b7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e6b7-117">Requirement</span></span> | <span data-ttu-id="8e6b7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8e6b7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e6b7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e6b7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8e6b7-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8e6b7-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8e6b7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e6b7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8e6b7-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8e6b7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8e6b7-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8e6b7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e6b7-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e6b7-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8e6b7-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="8e6b7-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8e6b7-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8e6b7-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8e6b7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8e6b7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e6b7-128"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8e6b7-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




