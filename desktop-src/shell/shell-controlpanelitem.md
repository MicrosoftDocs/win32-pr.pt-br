---
description: Executa o aplicativo do painel de controle ( \* . cpl) especificado.
title: Método Shell. ControlPanelItem (shldisp. h)
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
ms.openlocfilehash: dec27dab8bd37cc9c15e603c24a54d528cea331a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967991"
---
# <a name="shellcontrolpanelitem-method"></a><span data-ttu-id="670a5-103">Método Shell. ControlPanelItem</span><span class="sxs-lookup"><span data-stu-id="670a5-103">Shell.ControlPanelItem method</span></span>

<span data-ttu-id="670a5-104">Executa o aplicativo do painel de controle ( \* . cpl) especificado.</span><span class="sxs-lookup"><span data-stu-id="670a5-104">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="670a5-105">Se o aplicativo já estiver aberto, ele ativará a instância em execução.</span><span class="sxs-lookup"><span data-stu-id="670a5-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="670a5-106">A partir do Windows Vista, a maioria dos aplicativos do painel de controle são itens do Shell e não pode ser aberta com essa função.</span><span class="sxs-lookup"><span data-stu-id="670a5-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="670a5-107">Para abrir esses aplicativos do painel de controle, passe o nome canônico para control.exe.</span><span class="sxs-lookup"><span data-stu-id="670a5-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="670a5-108">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="670a5-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="670a5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="670a5-109">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="670a5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="670a5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="670a5-111">*bstrDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="670a5-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="670a5-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="670a5-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="670a5-113">O nome do arquivo do aplicativo do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="670a5-113">The Control Panel application's file name.</span></span> <span data-ttu-id="670a5-114">Todos os aplicativos do painel de controle têm a extensão. cpl.</span><span class="sxs-lookup"><span data-stu-id="670a5-114">All Control Panel applications have the .cpl extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="670a5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="670a5-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="670a5-116">JScript</span><span class="sxs-lookup"><span data-stu-id="670a5-116">JScript</span></span>

<span data-ttu-id="670a5-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="670a5-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="670a5-118">VB</span><span class="sxs-lookup"><span data-stu-id="670a5-118">VB</span></span>

<span data-ttu-id="670a5-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="670a5-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="670a5-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="670a5-120">Examples</span></span>

<span data-ttu-id="670a5-121">O exemplo a seguir usa **ControlPanelItem** para executar o item de **Propriedades de exibição** do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="670a5-121">The following example uses **ControlPanelItem** to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="670a5-122">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="670a5-122">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="670a5-123">JScript</span><span class="sxs-lookup"><span data-stu-id="670a5-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="670a5-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="670a5-124">VBScript:</span></span>


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



<span data-ttu-id="670a5-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="670a5-125">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="670a5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="670a5-126">Requirements</span></span>



| <span data-ttu-id="670a5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="670a5-127">Requirement</span></span> | <span data-ttu-id="670a5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="670a5-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="670a5-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="670a5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="670a5-130">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="670a5-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="670a5-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="670a5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="670a5-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="670a5-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="670a5-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="670a5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="670a5-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="670a5-134"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="670a5-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="670a5-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="670a5-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="670a5-136"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="670a5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="670a5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="670a5-138"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="670a5-138"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
