---
description: Cria uma caixa de diálogo que permite ao usuário selecionar uma pasta e, em seguida, retorna o objeto de pasta da pasta selecionada.
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: Método IShellDispatch. BrowseForFolder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e603bb08b4b98ba4008aa4ea162c9b59e5d42da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090847"
---
# <a name="ishelldispatchbrowseforfolder-method"></a><span data-ttu-id="33023-103">Método IShellDispatch. BrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="33023-103">IShellDispatch.BrowseForFolder method</span></span>

<span data-ttu-id="33023-104">Cria uma caixa de diálogo que permite ao usuário selecionar uma pasta e, em seguida, retorna o objeto de [**pasta**](folder.md) da pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="33023-104">Creates a dialog box that enables the user to select a folder and then returns the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="33023-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33023-105">Syntax</span></span>


```JScript
retVal = IShellDispatch.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

IShellDispatch.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a><span data-ttu-id="33023-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33023-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33023-107">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33023-107">*Hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33023-108">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="33023-108">Type: **Integer**</span></span>

<span data-ttu-id="33023-109">O identificador para a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="33023-109">The handle to the parent window of the dialog box.</span></span> <span data-ttu-id="33023-110">Esse valor pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="33023-110">This value can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="33023-111">*sTitle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33023-111">*sTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33023-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="33023-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="33023-113">Um valor de **cadeia de caracteres** que representa o título exibido dentro da caixa de diálogo de **procura** .</span><span class="sxs-lookup"><span data-stu-id="33023-113">A **String** value that represents the title displayed inside the **Browse** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="33023-114">*iOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33023-114">*iOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33023-115">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="33023-115">Type: **Integer**</span></span>

<span data-ttu-id="33023-116">Um valor **inteiro** que contém as opções para o método.</span><span class="sxs-lookup"><span data-stu-id="33023-116">An **Integer** value that contains the options for the method.</span></span> <span data-ttu-id="33023-117">Isso pode ser zero ou uma combinação dos valores listados no membro **ulFlags** da estrutura [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) .</span><span class="sxs-lookup"><span data-stu-id="33023-117">This can be zero or a combination of the values listed under the **ulFlags** member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="33023-118">*vRootFolder* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="33023-118">*vRootFolder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33023-119">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="33023-119">Type: **Variant**</span></span>

<span data-ttu-id="33023-120">A pasta raiz a ser usada na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="33023-120">The root folder to use in the dialog box.</span></span> <span data-ttu-id="33023-121">O usuário não pode navegar mais para cima na árvore do que essa pasta.</span><span class="sxs-lookup"><span data-stu-id="33023-121">The user cannot browse higher in the tree than this folder.</span></span> <span data-ttu-id="33023-122">Se esse valor não for especificado, a pasta raiz usada na caixa de diálogo será a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="33023-122">If this value is not specified, the root folder used in the dialog box is the desktop.</span></span> <span data-ttu-id="33023-123">Esse valor pode ser uma cadeia de caracteres que especifica o caminho da pasta ou um dos valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="33023-123">This value can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="33023-124">Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="33023-124">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="33023-125">Nesses casos, os valores numéricos devem ser usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="33023-125">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33023-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33023-126">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="33023-127">JScript</span><span class="sxs-lookup"><span data-stu-id="33023-127">JScript</span></span>

<span data-ttu-id="33023-128">Tipo: **pasta \* \***</span><span class="sxs-lookup"><span data-stu-id="33023-128">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="33023-129">Uma referência de objeto para o objeto de [**pasta**](folder.md) da pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="33023-129">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="33023-130">VB</span><span class="sxs-lookup"><span data-stu-id="33023-130">VB</span></span>

<span data-ttu-id="33023-131">Tipo: **pasta \* \***</span><span class="sxs-lookup"><span data-stu-id="33023-131">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="33023-132">Uma referência de objeto para o objeto de [**pasta**](folder.md) da pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="33023-132">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="33023-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="33023-133">Remarks</span></span>

<span data-ttu-id="33023-134">Esse método é implementado e acessado por meio do método [**shell. BrowseForFolder**](shell-browseforfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="33023-134">This method is implemented and accessed through the [**Shell.BrowseForFolder**](shell-browseforfolder.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="33023-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="33023-135">Examples</span></span>

<span data-ttu-id="33023-136">Os exemplos a seguir usam **BrowseForFolder** para exibir uma janela de procura intitulada "example" com raiz na pasta do Windows.</span><span class="sxs-lookup"><span data-stu-id="33023-136">The following examples use **BrowseForFolder** to display a browse window titled "Example" rooted at the Windows folder.</span></span> <span data-ttu-id="33023-137">O uso é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="33023-137">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="33023-138">JScript</span><span class="sxs-lookup"><span data-stu-id="33023-138">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



<span data-ttu-id="33023-139">VBScript</span><span class="sxs-lookup"><span data-stu-id="33023-139">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="33023-140">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="33023-140">Visual Basic:</span></span>


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="33023-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33023-141">Requirements</span></span>



| <span data-ttu-id="33023-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="33023-142">Requirement</span></span> | <span data-ttu-id="33023-143">Valor</span><span class="sxs-lookup"><span data-stu-id="33023-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33023-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33023-144">Minimum supported client</span></span><br/> | <span data-ttu-id="33023-145">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="33023-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="33023-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33023-146">Minimum supported server</span></span><br/> | <span data-ttu-id="33023-147">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="33023-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="33023-148">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="33023-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="33023-149"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33023-149"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="33023-150">INSERI</span><span class="sxs-lookup"><span data-stu-id="33023-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33023-151"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33023-151"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="33023-152">DLL</span><span class="sxs-lookup"><span data-stu-id="33023-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33023-153"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="33023-153"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
