---
description: Método Shell. Open – abre a pasta especificada.
ms.assetid: 96ed9360-fb8f-4f7e-aefb-4a63ec95df07
title: Método Shell. Open (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 36f8914be3fce6b461e5267562e6f3ef40aa5fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104224"
---
# <a name="shellopen-method"></a><span data-ttu-id="2dce1-103">Método Shell. Open</span><span class="sxs-lookup"><span data-stu-id="2dce1-103">Shell.Open method</span></span>

<span data-ttu-id="2dce1-104">Abre a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="2dce1-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dce1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2dce1-105">Syntax</span></span>


```JScript
iRetVal = Shell.Open(
  vDir
)
```


```VB

Shell.Open( _
  ByVal vDir As Variant _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="2dce1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2dce1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dce1-107">*vDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2dce1-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dce1-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="2dce1-108">Type: **Variant**</span></span>

<span data-ttu-id="2dce1-109">Uma cadeia de caracteres que especifica o caminho da pasta ou um dos valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="2dce1-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="2dce1-110">Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="2dce1-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="2dce1-111">Nesses casos, os valores numéricos devem ser usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="2dce1-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="2dce1-112">Se o *vDir* estiver definido como um dos [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) e a pasta especial não existir, essa função criará a pasta.</span><span class="sxs-lookup"><span data-stu-id="2dce1-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2dce1-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2dce1-113">Examples</span></span>

<span data-ttu-id="2dce1-114">O exemplo a seguir mostra a **abertura** em uso.</span><span class="sxs-lookup"><span data-stu-id="2dce1-114">The following example shows **Open** in use.</span></span> <span data-ttu-id="2dce1-115">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2dce1-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2dce1-116">JScript</span><span class="sxs-lookup"><span data-stu-id="2dce1-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objShell.Shell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="2dce1-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="2dce1-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Shell.Open("C:\\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2dce1-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2dce1-118">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2dce1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dce1-119">Requirements</span></span>



| <span data-ttu-id="2dce1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dce1-120">Requirement</span></span> | <span data-ttu-id="2dce1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2dce1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dce1-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dce1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2dce1-123">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2dce1-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2dce1-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dce1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2dce1-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2dce1-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2dce1-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2dce1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dce1-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dce1-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2dce1-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="2dce1-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2dce1-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2dce1-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2dce1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2dce1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dce1-131"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2dce1-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dce1-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2dce1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dce1-133">**Shell**</span><span class="sxs-lookup"><span data-stu-id="2dce1-133">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="2dce1-134">**Explorar**</span><span class="sxs-lookup"><span data-stu-id="2dce1-134">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




