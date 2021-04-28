---
description: Método IShellDispatch. NameSpace – cria e retorna um objeto de pasta para a pasta especificada.
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Método IShellDispatch. NameSpace (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d1db0a3969350b4be4bc32e027bf2000036e099f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100514"
---
# <a name="ishelldispatchnamespace-method"></a><span data-ttu-id="34620-103">Método IShellDispatch. NameSpace</span><span class="sxs-lookup"><span data-stu-id="34620-103">IShellDispatch.NameSpace method</span></span>

<span data-ttu-id="34620-104">Cria e retorna um objeto de [**pasta**](folder.md) para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="34620-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="34620-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34620-105">Syntax</span></span>


```JScript
retVal = IShellDispatch.NameSpace(
  vDir
)
```


```VB

IShellDispatch.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="34620-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34620-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34620-107">*vDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="34620-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34620-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="34620-108">Type: **Variant**</span></span>

<span data-ttu-id="34620-109">A pasta para a qual criar o objeto de [**pasta**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="34620-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="34620-110">Pode ser uma cadeia de caracteres que especifica o caminho da pasta ou um dos valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="34620-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="34620-111">Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="34620-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="34620-112">Nesses casos, os valores numéricos devem ser usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="34620-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34620-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="34620-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="34620-114">JScript</span><span class="sxs-lookup"><span data-stu-id="34620-114">JScript</span></span>

<span data-ttu-id="34620-115">Tipo: **[ **pasta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="34620-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="34620-116">Referência de objeto para o objeto de [**pasta**](folder.md) da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="34620-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="34620-117">Se a pasta não for criada com êxito, esse valor retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="34620-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="34620-118">VB</span><span class="sxs-lookup"><span data-stu-id="34620-118">VB</span></span>

<span data-ttu-id="34620-119">Tipo: **[ **pasta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="34620-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="34620-120">Referência de objeto para o objeto de [**pasta**](folder.md) da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="34620-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="34620-121">Se a pasta não for criada com êxito, esse valor retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="34620-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="remarks"></a><span data-ttu-id="34620-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="34620-122">Remarks</span></span>

<span data-ttu-id="34620-123">Esse método é implementado e acessado por meio do método [**shell. namespace**](shell-namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="34620-123">This method is implemented and accessed through the [**Shell.NameSpace**](shell-namespace.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="34620-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34620-124">Examples</span></span>

<span data-ttu-id="34620-125">Os exemplos a seguir mostram o uso do [**namespace**](shell-namespace.md) no JScript, no VBScript e no Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="34620-125">The following examples show the use of [**NameSpace**](shell-namespace.md) in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="34620-126">JScript</span><span class="sxs-lookup"><span data-stu-id="34620-126">JScript:</span></span>


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



<span data-ttu-id="34620-127">VBScript</span><span class="sxs-lookup"><span data-stu-id="34620-127">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="34620-128">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="34620-128">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="34620-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34620-129">Requirements</span></span>



| <span data-ttu-id="34620-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="34620-130">Requirement</span></span> | <span data-ttu-id="34620-131">Valor</span><span class="sxs-lookup"><span data-stu-id="34620-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34620-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34620-132">Minimum supported client</span></span><br/> | <span data-ttu-id="34620-133">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="34620-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="34620-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34620-134">Minimum supported server</span></span><br/> | <span data-ttu-id="34620-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="34620-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="34620-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="34620-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="34620-137"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="34620-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="34620-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="34620-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="34620-139"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="34620-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="34620-140">DLL</span><span class="sxs-lookup"><span data-stu-id="34620-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34620-141"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="34620-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




