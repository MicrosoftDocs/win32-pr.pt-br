---
description: Método Shell. AddToRecent – adiciona um arquivo à lista MRU (usada mais recentemente).
ms.assetid: 26D2AE5A-FC7E-4c7c-9F10-8D3D7AA236E7
title: Método Shell. AddToRecent (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.AddToRecent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 92ea7432c318939a01f86405ae33d8ac90b88c80
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083864"
---
# <a name="shelladdtorecent-method"></a><span data-ttu-id="10dcf-103">Método Shell. AddToRecent</span><span class="sxs-lookup"><span data-stu-id="10dcf-103">Shell.AddToRecent method</span></span>

<span data-ttu-id="10dcf-104">Adiciona um arquivo à lista MRU (usada mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="10dcf-104">Adds a file to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="10dcf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10dcf-105">Syntax</span></span>


```JScript
Shell.AddToRecent(
  varFile,
  [ bstrCategory ]
)
```


```VB

Shell.AddToRecent( _
  ByVal varFile As Variant, _
  [ ByVal bstrCategory As BSTR ] _
)
```





## <a name="parameters"></a><span data-ttu-id="10dcf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10dcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10dcf-107">*varFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10dcf-107">*varFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10dcf-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="10dcf-108">Type: **Variant**</span></span>

<span data-ttu-id="10dcf-109">Uma **cadeia de caracteres** que contém o caminho do arquivo a ser adicionado à lista de documentos usados recentemente.</span><span class="sxs-lookup"><span data-stu-id="10dcf-109">A **String** that contains the path of the file to add to the list of recently used documents.</span></span>

<span data-ttu-id="10dcf-110">**Windows Vista**: defina esse parâmetro como **nulo** para limpar a pasta documentos recentes.</span><span class="sxs-lookup"><span data-stu-id="10dcf-110">**Windows Vista**: Set this parameter to **null** to clear the recent documents folder.</span></span>

</dd> <dt>

<span data-ttu-id="10dcf-111">*bstrCategory* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="10dcf-111">*bstrCategory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="10dcf-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="10dcf-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="10dcf-113">Uma **cadeia de caracteres** que contém o nome da categoria na qual o arquivo será colocado.</span><span class="sxs-lookup"><span data-stu-id="10dcf-113">A **String** that contains the name of the category in which to place the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10dcf-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="10dcf-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="10dcf-115">JScript</span><span class="sxs-lookup"><span data-stu-id="10dcf-115">JScript</span></span>

<span data-ttu-id="10dcf-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="10dcf-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="10dcf-117">VB</span><span class="sxs-lookup"><span data-stu-id="10dcf-117">VB</span></span>

<span data-ttu-id="10dcf-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="10dcf-118">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="10dcf-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10dcf-119">Examples</span></span>

<span data-ttu-id="10dcf-120">Os exemplos a seguir mostram o uso de **AddToRecent** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="10dcf-120">The following examples show the use of **AddToRecent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="10dcf-121">JScript</span><span class="sxs-lookup"><span data-stu-id="10dcf-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch3AddToRecentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("system.ini");
            if (objFolderItem != null)
            {
                objShell.AddToRecent(objFolderItem.Path);
            }
        }
    }
</script>
```



<span data-ttu-id="10dcf-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="10dcf-122">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch3AddToRecentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
            
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder.ParseName("system.ini")
                if (not objFolderItem is nothing) then
                    objShell.AddToRecent (objFolderItem.Path)
                end if
                set objFolderItem = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="10dcf-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="10dcf-123">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch3AddToRecent()
    Dim objShell  As Shell
    Dim objFolder As Folder
    Dim ssfWINDOWS As Long

    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem

        Set objFolderItem = objFolder.ParseName("system.ini")
        If (Not objFolderItem Is Nothing) Then
            objShell.AddToRecent (objFolderItem.Path)
        End If
        Set objFolderItem = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="10dcf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10dcf-124">Requirements</span></span>



| <span data-ttu-id="10dcf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="10dcf-125">Requirement</span></span> | <span data-ttu-id="10dcf-126">Valor</span><span class="sxs-lookup"><span data-stu-id="10dcf-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10dcf-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10dcf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="10dcf-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="10dcf-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="10dcf-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10dcf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="10dcf-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10dcf-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="10dcf-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10dcf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="10dcf-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="10dcf-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="10dcf-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="10dcf-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="10dcf-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10dcf-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="10dcf-135">DLL</span><span class="sxs-lookup"><span data-stu-id="10dcf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10dcf-136"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="10dcf-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
