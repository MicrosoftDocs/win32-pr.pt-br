---
description: Contém o tamanho do item.
ms.assetid: 0eda405e-d54f-48d2-a060-a1fdcdb23785
title: Propriedade FolderItem. Size (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Size
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5d44d1c1ddd9b46f768f218250802562f9a36312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501154"
---
# <a name="folderitemsize-property"></a><span data-ttu-id="5895b-103">Propriedade FolderItem. Size</span><span class="sxs-lookup"><span data-stu-id="5895b-103">FolderItem.Size property</span></span>

<span data-ttu-id="5895b-104">Contém o tamanho do item.</span><span class="sxs-lookup"><span data-stu-id="5895b-104">Contains the item's size.</span></span>

<span data-ttu-id="5895b-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5895b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5895b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5895b-106">Syntax</span></span>


```JScript
iSize = FolderItem.Size
```



## <a name="property-value"></a><span data-ttu-id="5895b-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5895b-107">Property value</span></span>

<span data-ttu-id="5895b-108">Um **inteiro** que recebe o tamanho do item.</span><span class="sxs-lookup"><span data-stu-id="5895b-108">An **Integer** that receives the item's size.</span></span>

## <a name="examples"></a><span data-ttu-id="5895b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5895b-109">Examples</span></span>

<span data-ttu-id="5895b-110">O exemplo a seguir usa **tamanho** para recuperar o tamanho do arquivo executável do bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="5895b-110">The following example uses **Size** to retrieve the size of the Notepad executable file.</span></span> <span data-ttu-id="5895b-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5895b-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5895b-112">JScript</span><span class="sxs-lookup"><span data-stu-id="5895b-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemSizeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.Size;
            }
        }
    }
</script>
```



<span data-ttu-id="5895b-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="5895b-113">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnFolderItemSizeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.Size
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="5895b-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5895b-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemSizeVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.Size
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5895b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5895b-115">Requirements</span></span>



| <span data-ttu-id="5895b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5895b-116">Requirement</span></span> | <span data-ttu-id="5895b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5895b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5895b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5895b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5895b-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5895b-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5895b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5895b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5895b-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5895b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5895b-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5895b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5895b-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5895b-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5895b-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="5895b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5895b-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5895b-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5895b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5895b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5895b-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5895b-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




