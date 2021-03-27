---
description: Abre uma pasta especificada em uma janela do Windows Explorer.
ms.assetid: DB434D02-56B2-4e8f-9E43-BBF47C7BE377
title: Método IShellDispatch. Explore (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1ae29b4962dcac1be0b7ea23808e36ce005cb62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967541"
---
# <a name="ishelldispatchexplore-method"></a><span data-ttu-id="cc1ea-103">Método IShellDispatch. Explore</span><span class="sxs-lookup"><span data-stu-id="cc1ea-103">IShellDispatch.Explore method</span></span>

<span data-ttu-id="cc1ea-104">Abre uma pasta especificada em uma janela do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="cc1ea-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc1ea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc1ea-105">Syntax</span></span>


```JScript
IShellDispatch.Explore(
  vDir
)
```


```VB

IShellDispatch.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="cc1ea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc1ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc1ea-107">*vDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc1ea-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1ea-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="cc1ea-108">Type: **Variant**</span></span>

<span data-ttu-id="cc1ea-109">A pasta a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="cc1ea-109">The folder to be displayed.</span></span> <span data-ttu-id="cc1ea-110">Pode ser uma cadeia de caracteres que especifica o caminho da pasta ou um dos valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="cc1ea-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="cc1ea-111">Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="cc1ea-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="cc1ea-112">Nesses casos, os valores numéricos devem ser usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="cc1ea-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc1ea-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc1ea-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cc1ea-114">JScript</span><span class="sxs-lookup"><span data-stu-id="cc1ea-114">JScript</span></span>

<span data-ttu-id="cc1ea-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cc1ea-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="cc1ea-116">VB</span><span class="sxs-lookup"><span data-stu-id="cc1ea-116">VB</span></span>

<span data-ttu-id="cc1ea-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cc1ea-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc1ea-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc1ea-118">Remarks</span></span>

<span data-ttu-id="cc1ea-119">Esse método é implementado e acessado por meio do método [**shell. Explore**](shell-explore.md) .</span><span class="sxs-lookup"><span data-stu-id="cc1ea-119">This method is implemented and accessed through the [**Shell.Explore**](shell-explore.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="cc1ea-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cc1ea-120">Examples</span></span>

<span data-ttu-id="cc1ea-121">Os exemplos a seguir mostram o uso de **explorar** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cc1ea-121">The following examples show the use of **Explore** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cc1ea-122">JScript</span><span class="sxs-lookup"><span data-stu-id="cc1ea-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Explore("C:\\");
    }
</script>
```



<span data-ttu-id="cc1ea-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="cc1ea-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="cc1ea-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cc1ea-124">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cc1ea-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc1ea-125">Requirements</span></span>



| <span data-ttu-id="cc1ea-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc1ea-126">Requirement</span></span> | <span data-ttu-id="cc1ea-127">Valor</span><span class="sxs-lookup"><span data-stu-id="cc1ea-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1ea-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc1ea-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cc1ea-129">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cc1ea-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cc1ea-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc1ea-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cc1ea-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cc1ea-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cc1ea-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cc1ea-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc1ea-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc1ea-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cc1ea-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="cc1ea-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cc1ea-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cc1ea-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cc1ea-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cc1ea-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc1ea-137"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="cc1ea-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




