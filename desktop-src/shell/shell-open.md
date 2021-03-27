---
description: Abre a pasta especificada.
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
ms.openlocfilehash: 3572f48a7b129500c38c3c0227ba479ecb775067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828902"
---
# <a name="shellopen-method"></a><span data-ttu-id="3d1c3-103">Método Shell. Open</span><span class="sxs-lookup"><span data-stu-id="3d1c3-103">Shell.Open method</span></span>

<span data-ttu-id="3d1c3-104">Abre a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="3d1c3-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d1c3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d1c3-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="3d1c3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d1c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d1c3-107">*vDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3d1c3-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d1c3-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="3d1c3-108">Type: **Variant**</span></span>

<span data-ttu-id="3d1c3-109">Uma cadeia de caracteres que especifica o caminho da pasta ou um dos valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="3d1c3-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="3d1c3-110">Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="3d1c3-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="3d1c3-111">Nesses casos, os valores numéricos devem ser usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="3d1c3-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="3d1c3-112">Se o *vDir* estiver definido como um dos [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) e a pasta especial não existir, essa função criará a pasta.</span><span class="sxs-lookup"><span data-stu-id="3d1c3-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3d1c3-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3d1c3-113">Examples</span></span>

<span data-ttu-id="3d1c3-114">O exemplo a seguir mostra a **abertura** em uso.</span><span class="sxs-lookup"><span data-stu-id="3d1c3-114">The following example shows **Open** in use.</span></span> <span data-ttu-id="3d1c3-115">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3d1c3-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3d1c3-116">JScript</span><span class="sxs-lookup"><span data-stu-id="3d1c3-116">JScript:</span></span>


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



<span data-ttu-id="3d1c3-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="3d1c3-117">VBScript:</span></span>


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



<span data-ttu-id="3d1c3-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3d1c3-118">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3d1c3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d1c3-119">Requirements</span></span>



| <span data-ttu-id="3d1c3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d1c3-120">Requirement</span></span> | <span data-ttu-id="3d1c3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3d1c3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1c3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d1c3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3d1c3-123">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3d1c3-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3d1c3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d1c3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3d1c3-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3d1c3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3d1c3-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3d1c3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d1c3-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d1c3-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3d1c3-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="3d1c3-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3d1c3-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3d1c3-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3d1c3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3d1c3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d1c3-131"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3d1c3-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d1c3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d1c3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1c3-133">**Shell**</span><span class="sxs-lookup"><span data-stu-id="3d1c3-133">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="3d1c3-134">**Explorar**</span><span class="sxs-lookup"><span data-stu-id="3d1c3-134">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




