---
description: Recupera detalhes sobre um item em uma pasta. Por exemplo, seu tamanho, tipo ou a hora de sua última modificação.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Método Folder. GetDetailsOf (shlobj \_ Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ab89f00f254778a2417644d894f1e9e81eb43cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920624"
---
# <a name="foldergetdetailsof-method"></a><span data-ttu-id="6b51f-104">Método Folder. GetDetailsOf</span><span class="sxs-lookup"><span data-stu-id="6b51f-104">Folder.GetDetailsOf method</span></span>

<span data-ttu-id="6b51f-105">Recupera detalhes sobre um item em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="6b51f-105">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="6b51f-106">Por exemplo, seu tamanho, tipo ou a hora de sua última modificação.</span><span class="sxs-lookup"><span data-stu-id="6b51f-106">For example, its size, type, or the time of its last modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b51f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b51f-107">Syntax</span></span>


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a><span data-ttu-id="6b51f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b51f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b51f-109">*vItem*</span><span class="sxs-lookup"><span data-stu-id="6b51f-109">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="6b51f-110">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="6b51f-110">Type: **Variant**</span></span>

<span data-ttu-id="6b51f-111">O item para o qual recuperar as informações.</span><span class="sxs-lookup"><span data-stu-id="6b51f-111">The item for which to retrieve the information.</span></span> <span data-ttu-id="6b51f-112">Deve ser um objeto [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6b51f-112">This must be a [**FolderItem**](folderitem.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="6b51f-113">*iColumn*</span><span class="sxs-lookup"><span data-stu-id="6b51f-113">*iColumn*</span></span> 
</dt> <dd>

<span data-ttu-id="6b51f-114">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="6b51f-114">Type: **Integer**</span></span>

<span data-ttu-id="6b51f-115">Um valor **inteiro** que especifica as informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="6b51f-115">An **Integer** value that specifies the information to be retrieved.</span></span> <span data-ttu-id="6b51f-116">As informações disponíveis para um item dependem da pasta na qual são exibidas.</span><span class="sxs-lookup"><span data-stu-id="6b51f-116">The information available for an item depends on the folder in which it is displayed.</span></span> <span data-ttu-id="6b51f-117">Esse valor corresponde ao número de coluna com base em zero exibido em uma exibição de Shell.</span><span class="sxs-lookup"><span data-stu-id="6b51f-117">This value corresponds to the zero-based column number that is displayed in a Shell view.</span></span> <span data-ttu-id="6b51f-118">Para um item no sistema de arquivos, isso pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6b51f-118">For an item in the file system, this can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="6b51f-119"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="6b51f-119">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6b51f-120">Recupera o nome do item.</span><span class="sxs-lookup"><span data-stu-id="6b51f-120">Retrieves the name of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="6b51f-121">(1)</span><span class="sxs-lookup"><span data-stu-id="6b51f-121">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6b51f-122">Recupera o tamanho do item.</span><span class="sxs-lookup"><span data-stu-id="6b51f-122">Retrieves the size of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="6b51f-123">(2)</span><span class="sxs-lookup"><span data-stu-id="6b51f-123">(2)</span></span>


</dt> <dd>

<span data-ttu-id="6b51f-124">Recupera o tipo do item.</span><span class="sxs-lookup"><span data-stu-id="6b51f-124">Retrieves the type of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="6b51f-125">(3)</span><span class="sxs-lookup"><span data-stu-id="6b51f-125">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6b51f-126">Recupera a data e a hora da última modificação do item.</span><span class="sxs-lookup"><span data-stu-id="6b51f-126">Retrieves the date and time that the item was last modified.</span></span>

</dd> <dt>



 <span data-ttu-id="6b51f-127">(4)</span><span class="sxs-lookup"><span data-stu-id="6b51f-127">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6b51f-128">Recupera os atributos do item.</span><span class="sxs-lookup"><span data-stu-id="6b51f-128">Retrieves the attributes of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="6b51f-129">(-1)</span><span class="sxs-lookup"><span data-stu-id="6b51f-129">(-1)</span></span>


</dt> <dd>

<span data-ttu-id="6b51f-130">Recupera as informações da dica de informações para o item.</span><span class="sxs-lookup"><span data-stu-id="6b51f-130">Retrieves the info tip information for the item.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b51f-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b51f-131">Return value</span></span>

<span data-ttu-id="6b51f-132">Tipo: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="6b51f-132">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="6b51f-133">Cadeia de caracteres que contém os detalhes recuperados.</span><span class="sxs-lookup"><span data-stu-id="6b51f-133">String containing the retrieved detail.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b51f-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b51f-134">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6b51f-135">Nem todos os métodos são implementados para todas as pastas.</span><span class="sxs-lookup"><span data-stu-id="6b51f-135">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="6b51f-136">Por exemplo, o método [_ *ParseName* \*](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="6b51f-136">For example, the [_ *ParseName*\*](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="6b51f-137">Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.</span><span class="sxs-lookup"><span data-stu-id="6b51f-137">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="6b51f-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b51f-138">Examples</span></span>

<span data-ttu-id="6b51f-139">O exemplo a seguir usa **GetDetailsOf** para recuperar o tipo do arquivo chamado Clock.avi.</span><span class="sxs-lookup"><span data-stu-id="6b51f-139">The following example uses **GetDetailsOf** to retrieve the type of the file named Clock.avi.</span></span> <span data-ttu-id="6b51f-140">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6b51f-140">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6b51f-141">JScript</span><span class="sxs-lookup"><span data-stu-id="6b51f-141">JScript:</span></span>


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



<span data-ttu-id="6b51f-142">VBScript</span><span class="sxs-lookup"><span data-stu-id="6b51f-142">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
            end if
            
            set objFolderItem = nothing
        end if
        
        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="6b51f-143">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6b51f-143">Visual Basic:</span></span>


```VB
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
    End If
    
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6b51f-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b51f-144">Requirements</span></span>



| <span data-ttu-id="6b51f-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b51f-145">Requirement</span></span> | <span data-ttu-id="6b51f-146">Valor</span><span class="sxs-lookup"><span data-stu-id="6b51f-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b51f-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b51f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6b51f-148">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6b51f-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6b51f-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b51f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6b51f-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6b51f-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6b51f-151">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6b51f-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b51f-152"><dt>Shlobj \_ Core. h (incluir shldisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b51f-152"><dt>Shlobj\_core.h (include Shldisp.h)</dt></span></span> </dl>  |
| <span data-ttu-id="6b51f-153">INSERI</span><span class="sxs-lookup"><span data-stu-id="6b51f-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b51f-154"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b51f-154"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6b51f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="6b51f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b51f-156"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6b51f-156"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
