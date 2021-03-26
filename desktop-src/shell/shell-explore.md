---
description: Abre uma pasta especificada em uma janela do Windows Explorer.
ms.assetid: a788a3c4-f316-4fae-9294-3872eee8f46a
title: Método Shell. Explore (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 00b597aea0121e5f87f51886e8019a1130a20584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922492"
---
# <a name="shellexplore-method"></a><span data-ttu-id="f65b2-103">Método Shell. Explore</span><span class="sxs-lookup"><span data-stu-id="f65b2-103">Shell.Explore method</span></span>

<span data-ttu-id="f65b2-104">Abre uma pasta especificada em uma janela do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="f65b2-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f65b2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f65b2-105">Syntax</span></span>


```JScript
Shell.Explore(
  vDir
)
```


```VB

Shell.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="f65b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f65b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f65b2-107">*vDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f65b2-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f65b2-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="f65b2-108">Type: **Variant**</span></span>

<span data-ttu-id="f65b2-109">A pasta a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="f65b2-109">The folder to be displayed.</span></span> <span data-ttu-id="f65b2-110">Pode ser uma cadeia de caracteres que especifica o caminho da pasta ou um dos valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="f65b2-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="f65b2-111">Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="f65b2-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="f65b2-112">Nesses casos, os valores numéricos devem ser usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="f65b2-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f65b2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f65b2-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f65b2-114">JScript</span><span class="sxs-lookup"><span data-stu-id="f65b2-114">JScript</span></span>

<span data-ttu-id="f65b2-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f65b2-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f65b2-116">VB</span><span class="sxs-lookup"><span data-stu-id="f65b2-116">VB</span></span>

<span data-ttu-id="f65b2-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f65b2-117">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="f65b2-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f65b2-118">Examples</span></span>

<span data-ttu-id="f65b2-119">O exemplo a seguir mostra a **exploração** em uso.</span><span class="sxs-lookup"><span data-stu-id="f65b2-119">The following example shows **Explore** in use.</span></span> <span data-ttu-id="f65b2-120">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f65b2-120">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f65b2-121">JScript</span><span class="sxs-lookup"><span data-stu-id="f65b2-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Explore("C:\\");
    }
</script>]]>
```



<span data-ttu-id="f65b2-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="f65b2-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f65b2-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f65b2-123">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f65b2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f65b2-124">Requirements</span></span>



| <span data-ttu-id="f65b2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f65b2-125">Requirement</span></span> | <span data-ttu-id="f65b2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f65b2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f65b2-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f65b2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f65b2-128">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f65b2-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f65b2-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f65b2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f65b2-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f65b2-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f65b2-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f65b2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f65b2-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f65b2-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f65b2-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="f65b2-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f65b2-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f65b2-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f65b2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f65b2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f65b2-136"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f65b2-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




