---
description: Método Shell. Explore – abre uma pasta especificada em uma janela do Windows Explorer.
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
ms.openlocfilehash: 9ec1756ad6743c5bbac36f56087e6f3820cbb624
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104324"
---
# <a name="shellexplore-method"></a><span data-ttu-id="f049a-103">Método Shell. Explore</span><span class="sxs-lookup"><span data-stu-id="f049a-103">Shell.Explore method</span></span>

<span data-ttu-id="f049a-104">Abre uma pasta especificada em uma janela do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="f049a-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f049a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f049a-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="f049a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f049a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f049a-107">*vDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f049a-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f049a-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="f049a-108">Type: **Variant**</span></span>

<span data-ttu-id="f049a-109">A pasta a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="f049a-109">The folder to be displayed.</span></span> <span data-ttu-id="f049a-110">Pode ser uma cadeia de caracteres que especifica o caminho da pasta ou um dos valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="f049a-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="f049a-111">Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="f049a-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="f049a-112">Nesses casos, os valores numéricos devem ser usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="f049a-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f049a-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f049a-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f049a-114">JScript</span><span class="sxs-lookup"><span data-stu-id="f049a-114">JScript</span></span>

<span data-ttu-id="f049a-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f049a-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f049a-116">VB</span><span class="sxs-lookup"><span data-stu-id="f049a-116">VB</span></span>

<span data-ttu-id="f049a-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f049a-117">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="f049a-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f049a-118">Examples</span></span>

<span data-ttu-id="f049a-119">O exemplo a seguir mostra a **exploração** em uso.</span><span class="sxs-lookup"><span data-stu-id="f049a-119">The following example shows **Explore** in use.</span></span> <span data-ttu-id="f049a-120">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f049a-120">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f049a-121">JScript</span><span class="sxs-lookup"><span data-stu-id="f049a-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Explore("C:\\");
    }
</script>]]>
```



<span data-ttu-id="f049a-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="f049a-122">VBScript:</span></span>


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



<span data-ttu-id="f049a-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f049a-123">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f049a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f049a-124">Requirements</span></span>



| <span data-ttu-id="f049a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f049a-125">Requirement</span></span> | <span data-ttu-id="f049a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f049a-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f049a-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f049a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f049a-128">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f049a-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f049a-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f049a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f049a-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f049a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f049a-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f049a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f049a-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f049a-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f049a-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="f049a-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f049a-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f049a-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f049a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f049a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f049a-136"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f049a-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




