---
description: Cria uma caixa de diálogo que permite ao usuário selecionar uma pasta e, em seguida, retorna o objeto de pasta da pasta selecionada.
title: Método Shell. BrowseForFolder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4cc44e5a-3578-448b-9b19-1b71e1ae2cb9
ms.openlocfilehash: 7e14dffbfb9ab3e18bd4d8e11ffaf4768ad53131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011264"
---
# <a name="shellbrowseforfolder-method"></a><span data-ttu-id="c9b2f-103">Método Shell. BrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="c9b2f-103">Shell.BrowseForFolder method</span></span>

<span data-ttu-id="c9b2f-104">Cria uma caixa de diálogo que permite ao usuário selecionar uma pasta e, em seguida, retorna o objeto de [**pasta**](folder.md) da pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-104">Creates a dialog box that enables the user to select a folder and then returns the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b2f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9b2f-105">Syntax</span></span>


```JScript
retVal = Shell.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

Shell.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a><span data-ttu-id="c9b2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9b2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9b2f-107">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9b2f-107">*Hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b2f-108">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="c9b2f-108">Type: **Integer**</span></span>

<span data-ttu-id="c9b2f-109">O identificador para a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-109">The handle to the parent window of the dialog box.</span></span> <span data-ttu-id="c9b2f-110">Esse valor pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-110">This value can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c9b2f-111">*sTitle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9b2f-111">*sTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b2f-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c9b2f-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c9b2f-113">Um valor de **cadeia de caracteres** que representa o título exibido dentro da caixa de diálogo de **procura** .</span><span class="sxs-lookup"><span data-stu-id="c9b2f-113">A **String** value that represents the title displayed inside the **Browse** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="c9b2f-114">*iOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9b2f-114">*iOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b2f-115">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="c9b2f-115">Type: **Integer**</span></span>

<span data-ttu-id="c9b2f-116">Um valor **inteiro** que contém as opções para o método.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-116">An **Integer** value that contains the options for the method.</span></span> <span data-ttu-id="c9b2f-117">Isso pode ser zero ou uma combinação dos valores listados no membro **ulFlags** da estrutura [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) .</span><span class="sxs-lookup"><span data-stu-id="c9b2f-117">This can be zero or a combination of the values listed under the **ulFlags** member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c9b2f-118">*vRootFolder* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c9b2f-118">*vRootFolder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b2f-119">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="c9b2f-119">Type: **Variant**</span></span>

<span data-ttu-id="c9b2f-120">A pasta raiz a ser usada na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-120">The root folder to use in the dialog box.</span></span> <span data-ttu-id="c9b2f-121">O usuário não pode navegar mais para cima na árvore do que essa pasta.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-121">The user cannot browse higher in the tree than this folder.</span></span> <span data-ttu-id="c9b2f-122">Se esse valor não for especificado, a pasta raiz usada na caixa de diálogo será a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-122">If this value is not specified, the root folder used in the dialog box is the desktop.</span></span> <span data-ttu-id="c9b2f-123">Esse valor pode ser uma cadeia de caracteres que especifica o caminho da pasta ou um dos valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="c9b2f-123">This value can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="c9b2f-124">Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-124">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="c9b2f-125">Nesses casos, os valores numéricos devem ser usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-125">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9b2f-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9b2f-126">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c9b2f-127">JScript</span><span class="sxs-lookup"><span data-stu-id="c9b2f-127">JScript</span></span>

<span data-ttu-id="c9b2f-128">Tipo: **pasta \* \***</span><span class="sxs-lookup"><span data-stu-id="c9b2f-128">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="c9b2f-129">Uma referência de objeto para o objeto de [**pasta**](folder.md) da pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-129">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="c9b2f-130">VB</span><span class="sxs-lookup"><span data-stu-id="c9b2f-130">VB</span></span>

<span data-ttu-id="c9b2f-131">Tipo: **pasta \* \***</span><span class="sxs-lookup"><span data-stu-id="c9b2f-131">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="c9b2f-132">Uma referência de objeto para o objeto de [**pasta**](folder.md) da pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-132">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="c9b2f-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9b2f-133">Examples</span></span>

<span data-ttu-id="c9b2f-134">O exemplo a seguir usa **BrowseForFolder** para exibir uma janela de procura intitulada "example" com raiz na pasta do Windows.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-134">The following example uses **BrowseForFolder** to display a browse window titled "Example" rooted at the Windows folder.</span></span> <span data-ttu-id="c9b2f-135">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c9b2f-135">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c9b2f-136">JScript</span><span class="sxs-lookup"><span data-stu-id="c9b2f-136">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



<span data-ttu-id="c9b2f-137">VBScript</span><span class="sxs-lookup"><span data-stu-id="c9b2f-137">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c9b2f-138">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c9b2f-138">Visual Basic:</span></span>


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c9b2f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9b2f-139">Requirements</span></span>



| <span data-ttu-id="c9b2f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9b2f-140">Requirement</span></span> | <span data-ttu-id="c9b2f-141">Valor</span><span class="sxs-lookup"><span data-stu-id="c9b2f-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b2f-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9b2f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c9b2f-143">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c9b2f-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c9b2f-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9b2f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c9b2f-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c9b2f-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c9b2f-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c9b2f-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9b2f-147"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9b2f-147"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c9b2f-148">INSERI</span><span class="sxs-lookup"><span data-stu-id="c9b2f-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9b2f-149"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9b2f-149"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c9b2f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="c9b2f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9b2f-151"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c9b2f-151"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
