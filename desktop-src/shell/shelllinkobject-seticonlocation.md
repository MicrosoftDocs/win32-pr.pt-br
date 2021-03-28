---
description: Define o local do ícone atribuído ao link.
ms.assetid: 257bb8e2-29fa-4d2f-ac2d-3497cf12959c
title: Método ShellLinkObject. SetIconLocation (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.SetIconLocation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 996f9648e9b9f59e1e84871abac1d6b37e2592d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989040"
---
# <a name="shelllinkobjectseticonlocation-method"></a><span data-ttu-id="78973-103">Método ShellLinkObject. SetIconLocation</span><span class="sxs-lookup"><span data-stu-id="78973-103">ShellLinkObject.SetIconLocation method</span></span>

<span data-ttu-id="78973-104">Define o local do ícone atribuído ao link.</span><span class="sxs-lookup"><span data-stu-id="78973-104">Sets the location of the icon assigned to the link.</span></span>

## <a name="syntax"></a><span data-ttu-id="78973-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78973-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.SetIconLocation(
  sPath,
  iIndex
)
```



## <a name="parameters"></a><span data-ttu-id="78973-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78973-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78973-107">*sPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78973-107">*sPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78973-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="78973-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="78973-109">O caminho totalmente qualificado do arquivo que contém o ícone.</span><span class="sxs-lookup"><span data-stu-id="78973-109">The fully qualified path of the file that contains the icon.</span></span>

</dd> <dt>

<span data-ttu-id="78973-110">*iIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78973-110">*iIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78973-111">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="78973-111">Type: **Integer**</span></span>

<span data-ttu-id="78973-112">O índice do ícone no arquivo especificado por *sPath*.</span><span class="sxs-lookup"><span data-stu-id="78973-112">The index of the icon in the file specified by *sPath*.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="78973-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="78973-113">Examples</span></span>

<span data-ttu-id="78973-114">O exemplo a seguir mostra o uso apropriado desse método para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="78973-114">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="78973-115">JScript</span><span class="sxs-lookup"><span data-stu-id="78973-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectSetIconLocationJ()
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
                    objShellLink.SetIconLocation(objShellLink.Path, 1);
                    objShellLink.Save();
                }
            }
        }
    }
</script>
```



<span data-ttu-id="78973-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="78973-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectSetIconLocationVB()
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
                                objShellLink.SetIconLocation objShellLink.Path, 1
                                objShellLink.Save
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



<span data-ttu-id="78973-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="78973-117">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectSetIconLocationVB()
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
                            objShellLink.SetIconLocation objShellLink.Path, 1
                            objShellLink.Save
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="78973-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78973-118">Requirements</span></span>



| <span data-ttu-id="78973-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="78973-119">Requirement</span></span> | <span data-ttu-id="78973-120">Valor</span><span class="sxs-lookup"><span data-stu-id="78973-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78973-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78973-121">Minimum supported client</span></span><br/> | <span data-ttu-id="78973-122">Somente aplicativos de área de trabalho do Windows 2000 Professional com SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="78973-122">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="78973-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78973-123">Minimum supported server</span></span><br/> | <span data-ttu-id="78973-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="78973-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="78973-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="78973-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="78973-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="78973-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="78973-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="78973-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78973-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78973-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="78973-129">DLL</span><span class="sxs-lookup"><span data-stu-id="78973-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78973-130"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="78973-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
