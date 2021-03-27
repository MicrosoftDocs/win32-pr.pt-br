---
description: Abre a pasta especificada.
ms.assetid: 30FE669A-4AFD-4dfa-9F62-E62E744469C7
title: Método IShellDispatch. Open (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d794020313ad776c1d538dc2acb909d562d32f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647546"
---
# <a name="ishelldispatchopen-method"></a><span data-ttu-id="e07a5-103">Método IShellDispatch. Open</span><span class="sxs-lookup"><span data-stu-id="e07a5-103">IShellDispatch.Open method</span></span>

<span data-ttu-id="e07a5-104">Abre a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="e07a5-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="e07a5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e07a5-105">Syntax</span></span>


```JScript
IShellDispatch.Open(
  vDir
)
```


```VB

IShellDispatch.Open( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="e07a5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e07a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e07a5-107">*vDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e07a5-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07a5-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="e07a5-108">Type: **Variant**</span></span>

<span data-ttu-id="e07a5-109">Uma cadeia de caracteres que especifica o caminho da pasta ou um dos valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="e07a5-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="e07a5-110">Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="e07a5-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="e07a5-111">Nesses casos, os valores numéricos devem ser usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="e07a5-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="e07a5-112">Se o *vDir* estiver definido como um dos [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) e a pasta especial não existir, essa função criará a pasta.</span><span class="sxs-lookup"><span data-stu-id="e07a5-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e07a5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e07a5-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e07a5-114">JScript</span><span class="sxs-lookup"><span data-stu-id="e07a5-114">JScript</span></span>

<span data-ttu-id="e07a5-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e07a5-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="e07a5-116">VB</span><span class="sxs-lookup"><span data-stu-id="e07a5-116">VB</span></span>

<span data-ttu-id="e07a5-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e07a5-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e07a5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e07a5-118">Remarks</span></span>

<span data-ttu-id="e07a5-119">Esse método é implementado e acessado por meio do método [**shell. Open**](shell-open.md) .</span><span class="sxs-lookup"><span data-stu-id="e07a5-119">This method is implemented and accessed through the [**Shell.Open**](shell-open.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="e07a5-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e07a5-120">Examples</span></span>

<span data-ttu-id="e07a5-121">Os exemplos a seguir mostram o uso de **Open** no JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e07a5-121">The following examples show the use of **Open** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e07a5-122">JScript</span><span class="sxs-lookup"><span data-stu-id="e07a5-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objshell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="e07a5-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="e07a5-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Open("C:\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e07a5-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e07a5-124">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e07a5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e07a5-125">Requirements</span></span>



| <span data-ttu-id="e07a5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e07a5-126">Requirement</span></span> | <span data-ttu-id="e07a5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e07a5-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e07a5-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e07a5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e07a5-129">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e07a5-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e07a5-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e07a5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e07a5-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e07a5-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e07a5-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e07a5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e07a5-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e07a5-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e07a5-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="e07a5-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e07a5-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e07a5-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e07a5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e07a5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e07a5-137"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e07a5-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e07a5-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e07a5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07a5-139">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="e07a5-139">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="e07a5-140">**Explorar**</span><span class="sxs-lookup"><span data-stu-id="e07a5-140">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




