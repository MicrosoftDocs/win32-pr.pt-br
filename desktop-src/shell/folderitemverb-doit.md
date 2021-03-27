---
description: Executa um verbo no FolderItem associado ao verbo.
ms.assetid: 92400fe9-e4d1-4bc9-b4ee-d2adaf38154f
title: Método FolderItemVerb. DoIt (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.DoIt
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0703b9403dfe9ff6600de68aaa710cd5a55c225a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967263"
---
# <a name="folderitemverbdoit-method"></a><span data-ttu-id="6f8b1-103">Método FolderItemVerb. DoIt</span><span class="sxs-lookup"><span data-stu-id="6f8b1-103">FolderItemVerb.DoIt method</span></span>

<span data-ttu-id="6f8b1-104">Executa um verbo no [**FolderItem**](folderitem.md) associado ao verbo.</span><span class="sxs-lookup"><span data-stu-id="6f8b1-104">Executes a verb on the [**FolderItem**](folderitem.md) associated with the verb.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f8b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f8b1-105">Syntax</span></span>


```JScript
FolderItemVerb.DoIt()
```



## <a name="parameters"></a><span data-ttu-id="6f8b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f8b1-106">Parameters</span></span>

<span data-ttu-id="6f8b1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6f8b1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f8b1-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f8b1-108">Return value</span></span>

<span data-ttu-id="6f8b1-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6f8b1-109">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="6f8b1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6f8b1-110">Examples</span></span>

<span data-ttu-id="6f8b1-111">O exemplo a seguir usa **doit** para executar o primeiro verbo na coleção de verbos para a qual a pasta de programas do usuário responde.</span><span class="sxs-lookup"><span data-stu-id="6f8b1-111">The following example uses **DoIt** to execute the first verb in the collection of verbs to which the user's Program folder responds.</span></span> <span data-ttu-id="6f8b1-112">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6f8b1-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6f8b1-113">JScript</span><span class="sxs-lookup"><span data-stu-id="6f8b1-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbDoItJ()
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
                objVerbs.Item(0).DoIt();
            }
        }
    }
</script>
```



<span data-ttu-id="6f8b1-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="6f8b1-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbDoItVB()
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
                        objVerbs.Item(0).DoIt
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="6f8b1-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6f8b1-115">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbDoItVB()
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
                objVerbs.Item(0).DoIt
            End If
        Set objVerbs = Nothing
    End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6f8b1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f8b1-116">Requirements</span></span>



| <span data-ttu-id="6f8b1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f8b1-117">Requirement</span></span> | <span data-ttu-id="6f8b1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6f8b1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f8b1-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f8b1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6f8b1-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6f8b1-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6f8b1-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f8b1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6f8b1-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f8b1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6f8b1-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6f8b1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f8b1-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f8b1-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6f8b1-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="6f8b1-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f8b1-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f8b1-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6f8b1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6f8b1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f8b1-128"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6f8b1-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




