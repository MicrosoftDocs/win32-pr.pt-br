---
description: Recupera o objeto FolderItem para um item especificado na coleção.
ms.assetid: 164f823d-12d9-4950-a881-63837c53760d
title: Método FolderItems. Item (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ed670ed4af3882e38faf2699429c3d1c076f3056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967272"
---
# <a name="folderitemsitem-method"></a><span data-ttu-id="ddf59-103">Método FolderItems. Item</span><span class="sxs-lookup"><span data-stu-id="ddf59-103">FolderItems.Item method</span></span>

<span data-ttu-id="ddf59-104">Recupera o objeto [**FolderItem**](folderitem.md) para um item especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="ddf59-104">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddf59-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ddf59-105">Syntax</span></span>


```JScript
FolderItems.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="ddf59-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddf59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddf59-107">*iIndex* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ddf59-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddf59-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="ddf59-108">Type: **Variant**</span></span>

<span data-ttu-id="ddf59-109">O índice com base em zero do item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="ddf59-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="ddf59-110">Esse valor deve ser menor que o valor da propriedade [**Count**](folderitems-count.md) .</span><span class="sxs-lookup"><span data-stu-id="ddf59-110">This value must be less than the value of the [**Count**](folderitems-count.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddf59-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ddf59-111">Return value</span></span>

<span data-ttu-id="ddf59-112">Uma referência de objeto para o objeto [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ddf59-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="ddf59-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ddf59-113">Examples</span></span>

<span data-ttu-id="ddf59-114">O exemplo a seguir usa **Item** para recuperar o objeto [**FolderItem**](folderitem.md) que representa o arquivo de Notepad.exe encontrado na pasta do Windows.</span><span class="sxs-lookup"><span data-stu-id="ddf59-114">The following example uses **Item** to retrieve the [**FolderItem**](folderitem.md) object representing the Notepad.exe file found in the Windows folder.</span></span> <span data-ttu-id="ddf59-115">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ddf59-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ddf59-116">JScript</span><span class="sxs-lookup"><span data-stu-id="ddf59-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var objFolderItem;
                
                objFolderItem = objFolderItems.Item(objFolderItems.Count - 1);
                alert(objFolderItem.Name);
            }
        }
    }
</script>
```



<span data-ttu-id="ddf59-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="ddf59-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim objFolderItem
                    
                    set objFolderItem = objFolderItems.Item
                        if (not objFolderItem is nothing) then
                            alert(objFolderItem.Name)
                        end if
                    set objFolderItem = nothing
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="ddf59-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ddf59-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsItemVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim objFolderItem As FolderItem
                    
                    Set objFolderItem = objFolderItems.Item("NOTEPAD.EXE")
                        If (Not objFolderItem Is Nothing) Then
                            Debug.Print objFolderItem.Path
                        End If
                    Set objFolderItem = Nothing
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ddf59-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddf59-119">Requirements</span></span>



| <span data-ttu-id="ddf59-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddf59-120">Requirement</span></span> | <span data-ttu-id="ddf59-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ddf59-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf59-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddf59-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ddf59-123">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ddf59-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ddf59-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddf59-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ddf59-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ddf59-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ddf59-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ddf59-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddf59-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddf59-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ddf59-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="ddf59-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ddf59-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ddf59-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ddf59-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ddf59-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddf59-131"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ddf59-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddf59-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddf59-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf59-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="ddf59-133">**FolderItems**</span></span>](folderitems.md)
</dt> </dl>

 

 




