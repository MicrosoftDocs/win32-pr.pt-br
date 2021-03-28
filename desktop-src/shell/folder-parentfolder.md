---
description: Contém o objeto da pasta pai.
ms.assetid: b832948c-f599-4ada-8760-9280b86abfed
title: Propriedade Folder. ParentFolder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParentFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 200d8f8c931bd81015f52226bed5a4e584951e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921679"
---
# <a name="folderparentfolder-property"></a><span data-ttu-id="2efa3-103">Propriedade Folder. ParentFolder</span><span class="sxs-lookup"><span data-stu-id="2efa3-103">Folder.ParentFolder property</span></span>

<span data-ttu-id="2efa3-104">Contém o objeto da [**pasta**](folder.md) pai.</span><span class="sxs-lookup"><span data-stu-id="2efa3-104">Contains the parent [**Folder**](folder.md) object.</span></span>

<span data-ttu-id="2efa3-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2efa3-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2efa3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2efa3-106">Syntax</span></span>


```JScript
ParentFolder = Folder.ParentFolder
```



## <a name="property-value"></a><span data-ttu-id="2efa3-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2efa3-107">Property value</span></span>

<span data-ttu-id="2efa3-108">Uma referência de objeto para o objeto ParentFolder.</span><span class="sxs-lookup"><span data-stu-id="2efa3-108">An object reference to the ParentFolder object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2efa3-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2efa3-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2efa3-110">Nem todos os métodos são implementados para todas as pastas.</span><span class="sxs-lookup"><span data-stu-id="2efa3-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="2efa3-111">Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="2efa3-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="2efa3-112">Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.</span><span class="sxs-lookup"><span data-stu-id="2efa3-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2efa3-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2efa3-113">Examples</span></span>

<span data-ttu-id="2efa3-114">O exemplo a seguir mostra o uso apropriado de **ParentFolder** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2efa3-114">The following example shows the proper usage of **ParentFolder** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2efa3-115">JScript</span><span class="sxs-lookup"><span data-stu-id="2efa3-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderParentFolderJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objParentFolder;
                
            objParentFolder = objFolder.ParentFolder;
            if (objParentFolder != null)
            {
                alert(objParentFolder.Title);
            }
        }
    }
</script>
```



<span data-ttu-id="2efa3-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="2efa3-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderParentFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objParentFolder
                        
                set objParentFolder = objFolder.ParentFolder
                if (not objParentFolder is nothing) then
                    alert(objParentFolder.Title)
                end if
                set objParentFolder = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2efa3-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2efa3-117">Visual Basic:</span></span>


```VB
Private Sub fnFolderParentFolderVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objParentFolder As Folder
                
        Set objParentFolder = objFolder.ParentFolder
        If (Not objParentFolder Is Nothing) Then
            Debug.Print objParentFolder.Title
        End If
        Set objParentFolder = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2efa3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2efa3-118">Requirements</span></span>



| <span data-ttu-id="2efa3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2efa3-119">Requirement</span></span> | <span data-ttu-id="2efa3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2efa3-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2efa3-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2efa3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2efa3-122">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2efa3-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2efa3-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2efa3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2efa3-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2efa3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2efa3-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2efa3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2efa3-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2efa3-126"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2efa3-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="2efa3-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2efa3-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2efa3-128"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2efa3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2efa3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2efa3-130"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2efa3-130"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




