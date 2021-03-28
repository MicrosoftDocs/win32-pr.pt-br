---
description: Contém o título da pasta.
ms.assetid: 95c064ff-4504-4e9c-80ac-47beca443ad4
title: Propriedade Folder. Title (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Title
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8fc66d231d49d724749ae79b248b4dca9d917acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967933"
---
# <a name="foldertitle-property"></a><span data-ttu-id="46631-103">Propriedade Folder. title</span><span class="sxs-lookup"><span data-stu-id="46631-103">Folder.Title property</span></span>

<span data-ttu-id="46631-104">Contém o título da pasta.</span><span class="sxs-lookup"><span data-stu-id="46631-104">Contains the title of the folder.</span></span>

<span data-ttu-id="46631-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="46631-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="46631-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46631-106">Syntax</span></span>


```JScript
strTitle = Folder.Title
```



## <a name="property-value"></a><span data-ttu-id="46631-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="46631-107">Property value</span></span>

<span data-ttu-id="46631-108">Uma cadeia de caracteres que contém o título do objeto.</span><span class="sxs-lookup"><span data-stu-id="46631-108">A string containing the object's title.</span></span>

## <a name="remarks"></a><span data-ttu-id="46631-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="46631-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46631-110">Nem todos os métodos são implementados para todas as pastas.</span><span class="sxs-lookup"><span data-stu-id="46631-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="46631-111">Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="46631-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="46631-112">Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.</span><span class="sxs-lookup"><span data-stu-id="46631-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="46631-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46631-113">Examples</span></span>

<span data-ttu-id="46631-114">O exemplo a seguir usa **título** para recuperar o título da pasta que contém os grupos de programas do usuário (geralmente "programas").</span><span class="sxs-lookup"><span data-stu-id="46631-114">The following example uses **Title** to retrieve the title of the folder holding the user's program groups (usually "Programs").</span></span> <span data-ttu-id="46631-115">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="46631-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="46631-116">JScript</span><span class="sxs-lookup"><span data-stu-id="46631-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderTitleJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="46631-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="46631-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderTitleVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                alert(objFolder.Title)
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="46631-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="46631-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderTitleVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="46631-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46631-119">Requirements</span></span>



| <span data-ttu-id="46631-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="46631-120">Requirement</span></span> | <span data-ttu-id="46631-121">Valor</span><span class="sxs-lookup"><span data-stu-id="46631-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46631-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46631-122">Minimum supported client</span></span><br/> | <span data-ttu-id="46631-123">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="46631-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="46631-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46631-124">Minimum supported server</span></span><br/> | <span data-ttu-id="46631-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46631-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="46631-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="46631-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="46631-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="46631-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="46631-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="46631-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46631-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46631-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="46631-130">DLL</span><span class="sxs-lookup"><span data-stu-id="46631-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46631-131"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="46631-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




