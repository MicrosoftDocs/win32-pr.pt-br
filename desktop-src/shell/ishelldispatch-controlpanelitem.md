---
description: Executa o aplicativo Painel de Controle especificado.
title: Método IShellDispatch.ControlPanelItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9A9B6B3F-FBBC-4e76-8018-8858B6392276
ms.openlocfilehash: 1a1c024b316472be00f119485326b704a4fe8dd0
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842837"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a><span data-ttu-id="0ac34-103">Método IShellDispatch.ControlPanelItem</span><span class="sxs-lookup"><span data-stu-id="0ac34-103">IShellDispatch.ControlPanelItem method</span></span>

<span data-ttu-id="0ac34-104">Executa o aplicativo Painel de Controle especificado.</span><span class="sxs-lookup"><span data-stu-id="0ac34-104">Runs the specified Control Panel application.</span></span> <span data-ttu-id="0ac34-105">Se o aplicativo já estiver aberto, ele ativará a instância em execução.</span><span class="sxs-lookup"><span data-stu-id="0ac34-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="0ac34-106">A partir do Windows Vista, a maioria Painel de Controle aplicativos são itens do Shell e não podem ser abertos com essa função.</span><span class="sxs-lookup"><span data-stu-id="0ac34-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="0ac34-107">Para abrir esses Painel de Controle aplicativos, passe o nome canônico para control.exe.</span><span class="sxs-lookup"><span data-stu-id="0ac34-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="0ac34-108">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0ac34-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="0ac34-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ac34-109">Syntax</span></span>


```JScript
IShellDispatch.ControlPanelItem(
  bstrDir
)
```


```VB

IShellDispatch.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="0ac34-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ac34-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac34-111">*bstrDir* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="0ac34-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac34-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="0ac34-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="0ac34-113">O Painel de Controle nome do arquivo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0ac34-113">The Control Panel application's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ac34-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ac34-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0ac34-115">JScript</span><span class="sxs-lookup"><span data-stu-id="0ac34-115">JScript</span></span>

<span data-ttu-id="0ac34-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0ac34-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="0ac34-117">VB</span><span class="sxs-lookup"><span data-stu-id="0ac34-117">VB</span></span>

<span data-ttu-id="0ac34-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0ac34-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ac34-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ac34-119">Remarks</span></span>

<span data-ttu-id="0ac34-120">Esse método é implementado e acessado por meio do [**método Shell.ControlPanelItem.**](shell-controlpanelitem.md)</span><span class="sxs-lookup"><span data-stu-id="0ac34-120">This method is implemented and accessed through the [**Shell.ControlPanelItem**](shell-controlpanelitem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="0ac34-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0ac34-121">Examples</span></span>

<span data-ttu-id="0ac34-122">Os exemplos a seguir usam [**ControlPanelItem**](shell-controlpanelitem.md) para executar o Painel de Controle **do** Propriedades de Vídeo item.</span><span class="sxs-lookup"><span data-stu-id="0ac34-122">The following examples use [**ControlPanelItem**](shell-controlpanelitem.md) to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="0ac34-123">O uso é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0ac34-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0ac34-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="0ac34-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="0ac34-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="0ac34-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Shell_ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="0ac34-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="0ac34-126">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0ac34-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ac34-127">Requirements</span></span>



| <span data-ttu-id="0ac34-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ac34-128">Requirement</span></span> | <span data-ttu-id="0ac34-129">Valor</span><span class="sxs-lookup"><span data-stu-id="0ac34-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac34-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ac34-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac34-131">Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0ac34-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0ac34-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ac34-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac34-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0ac34-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0ac34-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0ac34-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ac34-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="0ac34-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0ac34-136">Idl</span><span class="sxs-lookup"><span data-stu-id="0ac34-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ac34-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ac34-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0ac34-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0ac34-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ac34-139"><dt>Shell32.dll (versão 4.71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="0ac34-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
