---
description: Obtém o valor de uma propriedade do conjunto de propriedades de um item. A propriedade pode ser especificada por nome ou pelo identificador de formato do conjunto de Propriedades (FMTID) e pelo identificador de propriedade (PID).
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: Método ShellFolderItem. Extended (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.ExtendedProperty
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 614e42512b17a0d8a6950ac96914128b8746c685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968122"
---
# <a name="shellfolderitemextendedproperty-method"></a><span data-ttu-id="7cd0c-104">Método ShellFolderItem. Extended</span><span class="sxs-lookup"><span data-stu-id="7cd0c-104">ShellFolderItem.ExtendedProperty method</span></span>

<span data-ttu-id="7cd0c-105">Obtém o valor de uma propriedade do conjunto de propriedades de um item.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-105">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="7cd0c-106">A propriedade pode ser especificada por nome ou pelo identificador de formato do conjunto de Propriedades (FMTID) e pelo identificador de propriedade (PID).</span><span class="sxs-lookup"><span data-stu-id="7cd0c-106">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd0c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cd0c-107">Syntax</span></span>


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a><span data-ttu-id="7cd0c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cd0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd0c-109">*sPropName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7cd0c-109">*sPropName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd0c-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="7cd0c-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="7cd0c-111">Um valor de **cadeia de caracteres** que especifica a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-111">A **String** value that specifies the property.</span></span> <span data-ttu-id="7cd0c-112">Consulte a seção comentários para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-112">See the Remarks section for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd0c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7cd0c-113">Return value</span></span>

<span data-ttu-id="7cd0c-114">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="7cd0c-114">Type: \**Variant\** _</span></span>

<span data-ttu-id="7cd0c-115">Quando esse método retornar, conterá o valor da propriedade, se existir para o item especificado.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-115">When this method returns, contains the value of the property, if it exists for the specified item.</span></span> <span data-ttu-id="7cd0c-116">O valor terá uma digitação completa — por exemplo, datas são retornadas como datas, não cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-116">The value will have full typing—for example, dates are returned as dates, not strings.</span></span>

<span data-ttu-id="7cd0c-117">Esse método retornará uma cadeia de caracteres de comprimento zero se a propriedade for válida, mas não existir para o item especificado, ou então um código de erro.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-117">This method returns a zero-length string if the property is valid but does not exist for the specified item, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd0c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cd0c-118">Remarks</span></span>

<span data-ttu-id="7cd0c-119">Há duas maneiras de especificar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-119">There are two ways to specify a property.</span></span> <span data-ttu-id="7cd0c-120">A primeira é atribuir o nome conhecido da propriedade, como "autor" ou "data", a _sPropName \*.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-120">The first is to assign the property's well-known name, such as "Author" or "Date", to _sPropName\*.</span></span> <span data-ttu-id="7cd0c-121">No entanto, cada propriedade é um membro de um conjunto de propriedades de Component Object Model (COM) e também pode ser identificada especificando sua ID de formato (FMTID) e ID de propriedade (PID).</span><span class="sxs-lookup"><span data-stu-id="7cd0c-121">However, each property is a member of a Component Object Model (COM) property set and can also be identified by specifying its format ID (FMTID) and property ID (PID).</span></span> <span data-ttu-id="7cd0c-122">Um [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) é um GUID que identifica o conjunto de propriedades e um [**pid**](../stg/structured-storage-serialized-property-set-format.md) é um inteiro que identifica uma propriedade específica dentro do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-122">An [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) is a GUID that identifies the property set, and a [**PID**](../stg/structured-storage-serialized-property-set-format.md) is an integer that identifies a particular property within the property set.</span></span>

<span data-ttu-id="7cd0c-123">Especificar uma propriedade por seus valores FMTID/PID é geralmente mais eficiente do que usar seu nome.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-123">Specifying a property by its FMTID/PID values is usually more efficient than using its name.</span></span> <span data-ttu-id="7cd0c-124">Para usar os valores de FMTID/PID de uma propriedade com **Extendeproperty**, eles devem ser combinados em um scid.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-124">To use a property's FMTID/PID values with **ExtendedProperty**, they must be combined into an SCID.</span></span> <span data-ttu-id="7cd0c-125">Um SCID é uma cadeia de caracteres que contém os valores FMTID/PID no formato "*FMTID \* \* PID*", em que FMTID é a forma de cadeia de caracteres do GUID do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-125">An SCID is a string that contains the FMTID/PID values in the form "*FMTID\*\*PID*", where the FMTID is the string form of the property set's GUID.</span></span> <span data-ttu-id="7cd0c-126">Por exemplo, o SCID da propriedade autor do conjunto de propriedades de informações de resumo é "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span><span class="sxs-lookup"><span data-stu-id="7cd0c-126">For example, the SCID of the summary information property set's author property is "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span></span>

<span data-ttu-id="7cd0c-127">Para obter uma lista de FMTIDs e PIDs que atualmente têm suporte no Shell, consulte [**SHCOLUMNID**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="7cd0c-127">For a list of FMTIDs and PIDs that are currently supported by the Shell, see [**SHCOLUMNID**](./objects.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7cd0c-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7cd0c-128">Examples</span></span>

<span data-ttu-id="7cd0c-129">Este código de exemplo ilustra como usar o **Extended** para recuperar as propriedades "title" e "Author" de um documento do Word.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-129">This sample code illustrates how to use **ExtendedProperty** to retrieve the "Title" and "Author" properties from a Word document.</span></span> <span data-ttu-id="7cd0c-130">Depois que você tiver o objeto [**ShellFolderItem**](shellfolderitem-object.md) associado ao arquivo, *fiWordDoc* neste exemplo, recupere o valor da propriedade, passando seu nome para **Extended**.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-130">Once you have the [**ShellFolderItem**](shellfolderitem-object.md) object associated with the file, *fiWordDoc* in this example, retrieve the property's value by passing its name to **ExtendedProperty**.</span></span>


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



<span data-ttu-id="7cd0c-131">Uma abordagem mais rápida e eficiente é passar um scid para o **Extended**.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-131">A faster and more efficient approach is to pass an SCID to **ExtendedProperty**.</span></span>


```none
...
FMTID_SummaryInfo="{F29F85E0-4FF9-1068-AB91-08002B27B3D9}"
PID_TITLE="2"
PID_AUTHOR="4"
SCID_TITLE=FMTID_SummaryInfo+" "+PID_TITLE
SCID_AUTHOR=FMTID_SummaryInfo+" "+PID_AUTHOR
Doc_Title=fiWordDoc.ExtendedProperty(SCID_TITLE)
Doc_Author=fiWordDoc.ExtendedProperty(SCID_AUTHOR)
...
```



<span data-ttu-id="7cd0c-132">Os exemplos a seguir mostram o uso apropriado desse método para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7cd0c-132">The following examples show the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7cd0c-133">JScript</span><span class="sxs-lookup"><span data-stu-id="7cd0c-133">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2ExtendedPropertyJ()
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
                var szReturn = "";
                
                szReturn = objFolderItem.ExtendedProperty("infotip");
                alert(szReturn);
            }
        }
    }
</script>
```



<span data-ttu-id="7cd0c-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="7cd0c-134">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemExtendedPropertyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                    
                    szReturn = objFolderItem.ExtendedProperty("type")
                    alert(szReturn)
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7cd0c-135">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7cd0c-135">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2ExtendedPropertyVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem2.ExtendedProperty("size")
                    Debug.Print szReturn
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7cd0c-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cd0c-136">Requirements</span></span>



| <span data-ttu-id="7cd0c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cd0c-137">Requirement</span></span> | <span data-ttu-id="7cd0c-138">Valor</span><span class="sxs-lookup"><span data-stu-id="7cd0c-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd0c-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cd0c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd0c-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7cd0c-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7cd0c-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cd0c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd0c-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7cd0c-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7cd0c-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7cd0c-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cd0c-144"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cd0c-144"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7cd0c-145">INSERI</span><span class="sxs-lookup"><span data-stu-id="7cd0c-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7cd0c-146"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7cd0c-146"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7cd0c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd0c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cd0c-148"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7cd0c-148"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
