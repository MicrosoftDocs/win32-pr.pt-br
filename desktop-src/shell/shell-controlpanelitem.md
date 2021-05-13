---
description: Executa o aplicativo Painel de Controle ( \* .cpl) especificado.
title: Método Shell.ControlPanelItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 54979bbd-b36b-4b5b-a8a0-5f63e9526fa5
ms.openlocfilehash: 04d2493f5d0ec5b86d19689cb8e7c2a02a82e536
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841797"
---
# <a name="shellcontrolpanelitem-method"></a><span data-ttu-id="15418-103">Método Shell.ControlPanelItem</span><span class="sxs-lookup"><span data-stu-id="15418-103">Shell.ControlPanelItem method</span></span>

<span data-ttu-id="15418-104">Executa o aplicativo Painel de Controle ( \* .cpl) especificado.</span><span class="sxs-lookup"><span data-stu-id="15418-104">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="15418-105">Se o aplicativo já estiver aberto, ele ativará a instância em execução.</span><span class="sxs-lookup"><span data-stu-id="15418-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="15418-106">A partir do Windows Vista, a maioria Painel de Controle aplicativos são itens do Shell e não podem ser abertos com essa função.</span><span class="sxs-lookup"><span data-stu-id="15418-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="15418-107">Para abrir esses Painel de Controle aplicativos, passe o nome canônico para control.exe.</span><span class="sxs-lookup"><span data-stu-id="15418-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="15418-108">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="15418-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="15418-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="15418-109">Syntax</span></span>


```JScript
Shell.ControlPanelItem(
  bstrDir
)
```


```VB

Shell.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="15418-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15418-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15418-111">*bstrDir* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="15418-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15418-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="15418-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="15418-113">O Painel de Controle nome do arquivo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15418-113">The Control Panel application's file name.</span></span> <span data-ttu-id="15418-114">Todos Painel de Controle aplicativos têm a extensão .cpl.</span><span class="sxs-lookup"><span data-stu-id="15418-114">All Control Panel applications have the .cpl extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15418-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15418-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="15418-116">JScript</span><span class="sxs-lookup"><span data-stu-id="15418-116">JScript</span></span>

<span data-ttu-id="15418-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="15418-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="15418-118">VB</span><span class="sxs-lookup"><span data-stu-id="15418-118">VB</span></span>

<span data-ttu-id="15418-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="15418-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="15418-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="15418-120">Examples</span></span>

<span data-ttu-id="15418-121">O exemplo a seguir **usa ControlPanelItem** para executar o Painel de Controle **do** Propriedades de Vídeo item.</span><span class="sxs-lookup"><span data-stu-id="15418-121">The following example uses **ControlPanelItem** to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="15418-122">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="15418-122">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="15418-123">Jscript:</span><span class="sxs-lookup"><span data-stu-id="15418-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="15418-124">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="15418-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="15418-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="15418-125">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="15418-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15418-126">Requirements</span></span>



| <span data-ttu-id="15418-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="15418-127">Requirement</span></span> | <span data-ttu-id="15418-128">Valor</span><span class="sxs-lookup"><span data-stu-id="15418-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15418-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15418-129">Minimum supported client</span></span><br/> | <span data-ttu-id="15418-130">Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="15418-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="15418-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15418-131">Minimum supported server</span></span><br/> | <span data-ttu-id="15418-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15418-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="15418-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="15418-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="15418-134"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="15418-134"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="15418-135">Idl</span><span class="sxs-lookup"><span data-stu-id="15418-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15418-136"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="15418-136"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="15418-137">DLL</span><span class="sxs-lookup"><span data-stu-id="15418-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15418-138"><dt>Shell32.dll (versão 4.71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="15418-138"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
