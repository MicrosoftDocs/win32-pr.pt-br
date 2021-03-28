---
description: Cria e retorna um objeto de pasta para a pasta especificada.
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Método Shell. NameSpace (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 856a86efb4aca6ae7c1d4c8a3a81b5bc722a3963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169553"
---
# <a name="shellnamespace-method"></a><span data-ttu-id="dfc53-103">Método Shell. NameSpace</span><span class="sxs-lookup"><span data-stu-id="dfc53-103">Shell.NameSpace method</span></span>

<span data-ttu-id="dfc53-104">Cria e retorna um objeto de [**pasta**](folder.md) para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="dfc53-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfc53-105">Syntax</span></span>


```JScript
retVal = Shell.NameSpace(
  vDir
)
```


```VB

Shell.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="dfc53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfc53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfc53-107">*vDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dfc53-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfc53-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="dfc53-108">Type: **Variant**</span></span>

<span data-ttu-id="dfc53-109">A pasta para a qual criar o objeto de [**pasta**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="dfc53-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="dfc53-110">Pode ser uma cadeia de caracteres que especifica o caminho da pasta ou um dos valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="dfc53-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="dfc53-111">Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="dfc53-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="dfc53-112">Nesses casos, os valores numéricos devem ser usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="dfc53-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfc53-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dfc53-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="dfc53-114">JScript</span><span class="sxs-lookup"><span data-stu-id="dfc53-114">JScript</span></span>

<span data-ttu-id="dfc53-115">Tipo: **[ **pasta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="dfc53-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="dfc53-116">Referência de objeto para o objeto de [**pasta**](folder.md) da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="dfc53-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="dfc53-117">Se a pasta não for criada com êxito, esse valor retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfc53-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="dfc53-118">VB</span><span class="sxs-lookup"><span data-stu-id="dfc53-118">VB</span></span>

<span data-ttu-id="dfc53-119">Tipo: **[ **pasta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="dfc53-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="dfc53-120">Referência de objeto para o objeto de [**pasta**](folder.md) da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="dfc53-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="dfc53-121">Se a pasta não for criada com êxito, esse valor retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfc53-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="dfc53-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dfc53-122">Examples</span></span>

<span data-ttu-id="dfc53-123">O exemplo a seguir mostra o **namespace** em uso.</span><span class="sxs-lookup"><span data-stu-id="dfc53-123">The following example shows **NameSpace** in use.</span></span> <span data-ttu-id="dfc53-124">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dfc53-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="dfc53-125">JScript</span><span class="sxs-lookup"><span data-stu-id="dfc53-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="dfc53-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="dfc53-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="dfc53-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="dfc53-127">Visual Basic:</span></span>


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="dfc53-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfc53-128">Requirements</span></span>



| <span data-ttu-id="dfc53-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfc53-129">Requirement</span></span> | <span data-ttu-id="dfc53-130">Valor</span><span class="sxs-lookup"><span data-stu-id="dfc53-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfc53-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfc53-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dfc53-132">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dfc53-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dfc53-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfc53-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dfc53-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dfc53-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dfc53-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dfc53-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfc53-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfc53-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="dfc53-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="dfc53-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dfc53-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dfc53-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="dfc53-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dfc53-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfc53-140"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="dfc53-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




