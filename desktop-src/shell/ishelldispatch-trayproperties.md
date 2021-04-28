---
description: Método IShellDispatch. Trayproperties – exibe a barra de tarefas e a caixa de diálogo Propriedades do menu iniciar. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar Propriedades.
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
title: Método IShellDispatch. Trayproperties (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 424d25d7555090e4244d5cd22084171ca2a4fea9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086614"
---
# <a name="ishelldispatchtrayproperties-method"></a><span data-ttu-id="f6f08-104">Método IShellDispatch. Trayproperties</span><span class="sxs-lookup"><span data-stu-id="f6f08-104">IShellDispatch.TrayProperties method</span></span>

<span data-ttu-id="f6f08-105">Exibe a **barra de tarefas e a caixa de diálogo Propriedades do menu iniciar** .</span><span class="sxs-lookup"><span data-stu-id="f6f08-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="f6f08-106">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="f6f08-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6f08-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6f08-107">Syntax</span></span>


```JScript
IShellDispatch.TrayProperties()
```


```VB

IShellDispatch.TrayProperties()
```





## <a name="parameters"></a><span data-ttu-id="f6f08-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6f08-108">Parameters</span></span>

<span data-ttu-id="f6f08-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f6f08-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6f08-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f6f08-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f6f08-111">JScript</span><span class="sxs-lookup"><span data-stu-id="f6f08-111">JScript</span></span>

<span data-ttu-id="f6f08-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f6f08-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f6f08-113">VB</span><span class="sxs-lookup"><span data-stu-id="f6f08-113">VB</span></span>

<span data-ttu-id="f6f08-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f6f08-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6f08-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6f08-115">Remarks</span></span>

<span data-ttu-id="f6f08-116">Esse método é implementado e acessado por meio do método [**shell. trayproperties**](shell-trayproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="f6f08-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="f6f08-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6f08-117">Examples</span></span>

<span data-ttu-id="f6f08-118">Os exemplos a seguir mostram o uso de **trayproperties** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f6f08-118">The following examples show the use of **TrayProperties** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f6f08-119">JScript</span><span class="sxs-lookup"><span data-stu-id="f6f08-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>
```



<span data-ttu-id="f6f08-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="f6f08-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f6f08-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f6f08-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f6f08-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6f08-122">Requirements</span></span>



| <span data-ttu-id="f6f08-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6f08-123">Requirement</span></span> | <span data-ttu-id="f6f08-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f6f08-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f08-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6f08-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f6f08-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f6f08-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f6f08-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6f08-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f6f08-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6f08-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f6f08-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f6f08-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6f08-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f08-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f6f08-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="f6f08-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6f08-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6f08-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f6f08-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f6f08-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6f08-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f6f08-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




