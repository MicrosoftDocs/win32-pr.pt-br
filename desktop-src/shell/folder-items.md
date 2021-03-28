---
description: Recupera um objeto FolderItems que representa a coleção de itens na pasta.
ms.assetid: ef2965ec-c8ab-4108-8e5e-b4fd5370521a
title: Método Folder. Items (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Items
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3cfa0fcd2d8e2e51a67a362b33af34abf5b1427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296730"
---
# <a name="folderitems-method"></a><span data-ttu-id="43732-103">Método Folder. Items</span><span class="sxs-lookup"><span data-stu-id="43732-103">Folder.Items method</span></span>

<span data-ttu-id="43732-104">Recupera um objeto [**FolderItems**](folderitems.md) que representa a coleção de itens na pasta.</span><span class="sxs-lookup"><span data-stu-id="43732-104">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="43732-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43732-105">Syntax</span></span>


```JScript
retVal = Folder.Items()
```



## <a name="parameters"></a><span data-ttu-id="43732-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43732-106">Parameters</span></span>

<span data-ttu-id="43732-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="43732-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43732-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43732-108">Return value</span></span>

<span data-ttu-id="43732-109">Tipo: **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="43732-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="43732-110">Uma referência de objeto para o objeto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="43732-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="43732-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="43732-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="43732-112">Nem todos os métodos são implementados para todas as pastas.</span><span class="sxs-lookup"><span data-stu-id="43732-112">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="43732-113">Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="43732-113">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="43732-114">Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.</span><span class="sxs-lookup"><span data-stu-id="43732-114">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="43732-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="43732-115">Examples</span></span>

<span data-ttu-id="43732-116">O exemplo a seguir usa **itens** para determinar o número de itens na pasta C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="43732-116">The following example uses **Items** to determine the number of items in the C:\\Windows folder.</span></span> <span data-ttu-id="43732-117">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="43732-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="43732-118">JScript</span><span class="sxs-lookup"><span data-stu-id="43732-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectItemsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItems = new Object;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                document.write (objFolderItems.Count);
            }
        }
    }
</script>
```



<span data-ttu-id="43732-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="43732-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectItemsVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItems

            set objFolderItems = objFolder.Items

            if (not objFolderItems Is Nothing) then
                document.write objFolderItems.Count
            end if

            set objFolderItem = nothing
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="43732-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="43732-120">Visual Basic:</span></span>


```VB
Private Sub btnFolderObjectItems_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItems As FolderItems

        Set objFolderItems = objFolder.Items()

        If (Not objFolderItems Is Nothing) Then
            Dim vCount As Variant

            vCount = objFolderItems.Count
        End If

        Set objFolderItems = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="43732-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43732-121">Requirements</span></span>



| <span data-ttu-id="43732-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="43732-122">Requirement</span></span> | <span data-ttu-id="43732-123">Valor</span><span class="sxs-lookup"><span data-stu-id="43732-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43732-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43732-124">Minimum supported client</span></span><br/> | <span data-ttu-id="43732-125">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="43732-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="43732-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43732-126">Minimum supported server</span></span><br/> | <span data-ttu-id="43732-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43732-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="43732-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="43732-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="43732-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="43732-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="43732-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="43732-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43732-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43732-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="43732-132">DLL</span><span class="sxs-lookup"><span data-stu-id="43732-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43732-133"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="43732-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




