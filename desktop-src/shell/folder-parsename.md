---
description: Cria e retorna um objeto FolderItem que representa um item especificado.
ms.assetid: 3af7052c-fb81-4a96-9bf9-379b0365a376
title: Método Folder. ParseName (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParseName
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ea9a8090a794f23693ae4fef10556bc207f16531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646568"
---
# <a name="folderparsename-method"></a><span data-ttu-id="733c7-103">Método Folder. ParseName</span><span class="sxs-lookup"><span data-stu-id="733c7-103">Folder.ParseName method</span></span>

<span data-ttu-id="733c7-104">Cria e retorna um objeto [**FolderItem**](folderitem.md) que representa um item especificado.</span><span class="sxs-lookup"><span data-stu-id="733c7-104">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="733c7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="733c7-105">Syntax</span></span>


```JScript
retVal = Folder.ParseName(
  bName
)
```



## <a name="parameters"></a><span data-ttu-id="733c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="733c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733c7-107">*bName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="733c7-107">*bName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="733c7-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="733c7-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="733c7-109">Uma cadeia de caracteres que especifica o nome do item.</span><span class="sxs-lookup"><span data-stu-id="733c7-109">A string that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733c7-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="733c7-110">Return value</span></span>

<span data-ttu-id="733c7-111">Tipo: **[ **FolderItem**](folderitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="733c7-111">Type: **[**FolderItem**](folderitem.md)\*\***</span></span>

<span data-ttu-id="733c7-112">Uma referência de objeto para o objeto [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="733c7-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="733c7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="733c7-113">Remarks</span></span>

<span data-ttu-id="733c7-114">**ParseName** não deve ser usado para pastas virtuais, como meus documentos.</span><span class="sxs-lookup"><span data-stu-id="733c7-114">**ParseName** should not be used for virtual folders such as My Documents.</span></span>

## <a name="examples"></a><span data-ttu-id="733c7-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="733c7-115">Examples</span></span>

<span data-ttu-id="733c7-116">O exemplo a seguir usa **ParseName** para criar um objeto que representa o item de pasta Clock.avi na \\ pasta C: Windows.</span><span class="sxs-lookup"><span data-stu-id="733c7-116">The following example uses **ParseName** to create an object representing the folder item Clock.avi in the C:\\Windows folder.</span></span> <span data-ttu-id="733c7-117">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="733c7-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="733c7-118">JScript</span><span class="sxs-lookup"><span data-stu-id="733c7-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectParseNameJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="733c7-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="733c7-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectParseNameVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="733c7-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="733c7-120">Visual Basic:</span></span>


```VB
Private Sub btnParseName_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder.ParseName("clock.avi")
            'Add code here.
            Debug.Print "passed"
        Set objFolderItem = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="733c7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="733c7-121">Requirements</span></span>



| <span data-ttu-id="733c7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="733c7-122">Requirement</span></span> | <span data-ttu-id="733c7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="733c7-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="733c7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="733c7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="733c7-125">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="733c7-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="733c7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="733c7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="733c7-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="733c7-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="733c7-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="733c7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="733c7-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="733c7-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="733c7-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="733c7-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="733c7-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="733c7-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="733c7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="733c7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="733c7-133"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="733c7-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
