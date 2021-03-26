---
description: Obtém o local do ícone atribuído ao link.
ms.assetid: 3bb7f0f0-7ab9-41e6-b738-274efbcd52ab
title: Método ShellLinkObject. GetIconLocation (shlobj \_ Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.GetIconLocation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ef2f502d30116def68aa43269b3020d404ce177d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170693"
---
# <a name="shelllinkobjectgeticonlocation-method"></a><span data-ttu-id="04b7e-103">Método ShellLinkObject. GetIconLocation</span><span class="sxs-lookup"><span data-stu-id="04b7e-103">ShellLinkObject.GetIconLocation method</span></span>

<span data-ttu-id="04b7e-104">Obtém o local do ícone atribuído ao link.</span><span class="sxs-lookup"><span data-stu-id="04b7e-104">Gets the location of the icon assigned to the link.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b7e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04b7e-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.GetIconLocation(
  sPath
)
```



## <a name="parameters"></a><span data-ttu-id="04b7e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04b7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04b7e-107">*sPath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04b7e-107">*sPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04b7e-108">Tipo: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="04b7e-108">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="04b7e-109">Quando esse método retorna, ele contém o caminho totalmente qualificado do arquivo que contém o ícone.</span><span class="sxs-lookup"><span data-stu-id="04b7e-109">When this method returns, it holds the fully qualified path of the file that contains the icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04b7e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04b7e-110">Return value</span></span>

<span data-ttu-id="04b7e-111">Tipo: _*inteiro \**_</span><span class="sxs-lookup"><span data-stu-id="04b7e-111">Type: _*Integer\**_</span></span>

<span data-ttu-id="04b7e-112">Retorna o índice do ícone no arquivo especificado por _sPath \*.</span><span class="sxs-lookup"><span data-stu-id="04b7e-112">Returns the icon's index in the file specified by _sPath\*.</span></span>

## <a name="examples"></a><span data-ttu-id="04b7e-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="04b7e-113">Examples</span></span>

<span data-ttu-id="04b7e-114">O exemplo a seguir mostra o uso apropriado desse método para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="04b7e-114">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="04b7e-115">JScript</span><span class="sxs-lookup"><span data-stu-id="04b7e-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectGetIconLocationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    var nIcon;
                    
                    nIcon = objShellLink.GetIconLocation(objFolderItem.Path);
                    alert(nIcon);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="04b7e-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="04b7e-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectGetIconLocationVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                dim nIcon
                                
                                nIcon = objShellLink.GetIconLocation(objFolderItem.Path)
                                alert(nIcon)
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="04b7e-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="04b7e-117">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectGetIconLocationVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            Dim nIcon As Integer
                            
                            nIcon = objShellLink.GetIconLocation(objFolderItem.Path)
                            Debug.Print nIcon
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="04b7e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04b7e-118">Requirements</span></span>



| <span data-ttu-id="04b7e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="04b7e-119">Requirement</span></span> | <span data-ttu-id="04b7e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="04b7e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b7e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04b7e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="04b7e-122">Somente aplicativos de área de trabalho do Windows 2000 Professional com SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="04b7e-122">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="04b7e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04b7e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="04b7e-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="04b7e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="04b7e-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="04b7e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="04b7e-126"><dt>Shlobj \_ Core. h (incluir shldisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04b7e-126"><dt>Shlobj\_core.h (include Shldisp.h)</dt></span></span> </dl> |
| <span data-ttu-id="04b7e-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="04b7e-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04b7e-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04b7e-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="04b7e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="04b7e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04b7e-130"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="04b7e-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b7e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="04b7e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b7e-132">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="04b7e-132">**ShellLinkObject**</span></span>](shelllinkobject-object.md)
</dt> <dt>

[<span data-ttu-id="04b7e-133">**SetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="04b7e-133">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md)
</dt> </dl>

 

 
