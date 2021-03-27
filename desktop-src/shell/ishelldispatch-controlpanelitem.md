---
description: Executa o aplicativo do painel de controle especificado.
title: Método IShellDispatch. ControlPanelItem (shldisp. h)
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
ms.openlocfilehash: 72164ff76cbcf15703bc91160e6211b38015f989
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502089"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a><span data-ttu-id="27268-103">Método IShellDispatch. ControlPanelItem</span><span class="sxs-lookup"><span data-stu-id="27268-103">IShellDispatch.ControlPanelItem method</span></span>

<span data-ttu-id="27268-104">Executa o aplicativo do painel de controle especificado.</span><span class="sxs-lookup"><span data-stu-id="27268-104">Runs the specified Control Panel application.</span></span> <span data-ttu-id="27268-105">Se o aplicativo já estiver aberto, ele ativará a instância em execução.</span><span class="sxs-lookup"><span data-stu-id="27268-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="27268-106">A partir do Windows Vista, a maioria dos aplicativos do painel de controle são itens do Shell e não pode ser aberta com essa função.</span><span class="sxs-lookup"><span data-stu-id="27268-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="27268-107">Para abrir esses aplicativos do painel de controle, passe o nome canônico para control.exe.</span><span class="sxs-lookup"><span data-stu-id="27268-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="27268-108">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="27268-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="27268-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="27268-109">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="27268-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27268-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27268-111">*bstrDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27268-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27268-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="27268-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="27268-113">O nome do arquivo do aplicativo do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="27268-113">The Control Panel application's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27268-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27268-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="27268-115">JScript</span><span class="sxs-lookup"><span data-stu-id="27268-115">JScript</span></span>

<span data-ttu-id="27268-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="27268-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="27268-117">VB</span><span class="sxs-lookup"><span data-stu-id="27268-117">VB</span></span>

<span data-ttu-id="27268-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="27268-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="27268-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="27268-119">Remarks</span></span>

<span data-ttu-id="27268-120">Esse método é implementado e acessado por meio do método [**shell. ControlPanelItem**](shell-controlpanelitem.md) .</span><span class="sxs-lookup"><span data-stu-id="27268-120">This method is implemented and accessed through the [**Shell.ControlPanelItem**](shell-controlpanelitem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="27268-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="27268-121">Examples</span></span>

<span data-ttu-id="27268-122">Os exemplos a seguir usam [**ControlPanelItem**](shell-controlpanelitem.md) para executar o item de **Propriedades de exibição** do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="27268-122">The following examples use [**ControlPanelItem**](shell-controlpanelitem.md) to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="27268-123">O uso é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="27268-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="27268-124">JScript</span><span class="sxs-lookup"><span data-stu-id="27268-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="27268-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="27268-125">VBScript:</span></span>


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



<span data-ttu-id="27268-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="27268-126">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="27268-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27268-127">Requirements</span></span>



| <span data-ttu-id="27268-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="27268-128">Requirement</span></span> | <span data-ttu-id="27268-129">Valor</span><span class="sxs-lookup"><span data-stu-id="27268-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27268-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27268-130">Minimum supported client</span></span><br/> | <span data-ttu-id="27268-131">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="27268-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="27268-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27268-132">Minimum supported server</span></span><br/> | <span data-ttu-id="27268-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="27268-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="27268-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="27268-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="27268-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="27268-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="27268-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="27268-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="27268-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="27268-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="27268-138">DLL</span><span class="sxs-lookup"><span data-stu-id="27268-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27268-139"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="27268-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
