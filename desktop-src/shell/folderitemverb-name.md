---
description: Contém o nome do verbo.
ms.assetid: d18fddac-eb51-4031-a572-1bfef2f757a9
title: Propriedade FolderItemVerb.Name (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.Name
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5d352f02486f1d7304d4c474aa836401bfef635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967262"
---
# <a name="folderitemverbname-property"></a><span data-ttu-id="dc0b7-103">Propriedade FolderItemVerb.Name</span><span class="sxs-lookup"><span data-stu-id="dc0b7-103">FolderItemVerb.Name property</span></span>

<span data-ttu-id="dc0b7-104">Contém o nome do verbo.</span><span class="sxs-lookup"><span data-stu-id="dc0b7-104">Contains the verb's name.</span></span>

<span data-ttu-id="dc0b7-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="dc0b7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0b7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc0b7-106">Syntax</span></span>


```JScript
strName = FolderItemVerb.Name
```



## <a name="property-value"></a><span data-ttu-id="dc0b7-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="dc0b7-107">Property value</span></span>

<span data-ttu-id="dc0b7-108">Uma variável do tipo [**BSTR**](/previous-versions/windows/desktop/automat/bstr) que recebe a propriedade Name.</span><span class="sxs-lookup"><span data-stu-id="dc0b7-108">A variable of type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) that receives the Name property.</span></span>

## <a name="examples"></a><span data-ttu-id="dc0b7-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dc0b7-109">Examples</span></span>

<span data-ttu-id="dc0b7-110">O exemplo a seguir usa **Name** para recuperar o nome do primeiro item na coleção de verbos para a qual a pasta de programas do usuário responde.</span><span class="sxs-lookup"><span data-stu-id="dc0b7-110">The following example uses **Name** to retrieve the name of the first item in the collection of verbs to which the user's Program folder responds.</span></span> <span data-ttu-id="dc0b7-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dc0b7-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="dc0b7-112">JScript</span><span class="sxs-lookup"><span data-stu-id="dc0b7-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbNameJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objVerbs;
            
            objVerbs = objFolder.Self.Verbs();
            if (objVerbs != null)
            {
                var szReturn = "";
                
                szReturn = objVerbs.Item(0).Name;
                alert(szReturn);
            }
        }
    }
</script>
```



<span data-ttu-id="dc0b7-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="dc0b7-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbNameVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objVerbs
                
                set objVerbs = objFolder.Self.Verbs
                    if (not objVerbs is nothing) then
                        dim szReturn
                        
                        szReturn = objVerbs.Item(0).Name
                        alert(szReturn)
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="dc0b7-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="dc0b7-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbNameVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        
        Set objVerbs = objFolder2.Self.Verbs
            If (Not objVerbs Is Nothing) Then
                Dim szReturn As String
                
                szReturn = objVerbs.Item(0).Name
                Debug.Print szReturn
            End If
        Set objVerbs = Nothing
    End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="dc0b7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc0b7-115">Requirements</span></span>



| <span data-ttu-id="dc0b7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc0b7-116">Requirement</span></span> | <span data-ttu-id="dc0b7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dc0b7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc0b7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc0b7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dc0b7-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dc0b7-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dc0b7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc0b7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dc0b7-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dc0b7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dc0b7-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dc0b7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc0b7-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc0b7-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="dc0b7-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="dc0b7-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc0b7-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc0b7-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="dc0b7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dc0b7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc0b7-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="dc0b7-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
