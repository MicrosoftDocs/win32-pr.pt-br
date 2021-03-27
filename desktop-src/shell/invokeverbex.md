---
description: Executa um verbo em um item de Shell.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Método ShellFolderItem. InvokeVerbEx (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967552"
---
# <a name="shellfolderiteminvokeverbex-method"></a><span data-ttu-id="acbcc-103">Método ShellFolderItem. InvokeVerbEx</span><span class="sxs-lookup"><span data-stu-id="acbcc-103">ShellFolderItem.InvokeVerbEx method</span></span>

<span data-ttu-id="acbcc-104">Executa um verbo em um item de Shell.</span><span class="sxs-lookup"><span data-stu-id="acbcc-104">Executes a verb on a Shell item.</span></span>

## <a name="syntax"></a><span data-ttu-id="acbcc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acbcc-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="acbcc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acbcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acbcc-107">*vVerb* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="acbcc-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="acbcc-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="acbcc-108">Type: **Variant**</span></span>

<span data-ttu-id="acbcc-109">Uma **variante** que contém a cadeia de caracteres de verbo que corresponde ao comando a ser executado.</span><span class="sxs-lookup"><span data-stu-id="acbcc-109">A **Variant** that contains the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="acbcc-110">Deve ser um dos valores retornados pela propriedade [**Name**](folderitemverb-name.md) do item.</span><span class="sxs-lookup"><span data-stu-id="acbcc-110">It must be one of the values returned by the item's [**Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="acbcc-111">Se nenhum verbo for especificado, o verbo padrão será executado.</span><span class="sxs-lookup"><span data-stu-id="acbcc-111">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="acbcc-112">*vArgs* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="acbcc-112">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="acbcc-113">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="acbcc-113">Type: **Variant**</span></span>

<span data-ttu-id="acbcc-114">Uma **variante** que consiste em uma cadeia de caracteres com um ou mais argumentos para o comando especificado por *vVerb*.</span><span class="sxs-lookup"><span data-stu-id="acbcc-114">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="acbcc-115">O formato dessa cadeia de caracteres depende do verbo específico.</span><span class="sxs-lookup"><span data-stu-id="acbcc-115">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acbcc-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="acbcc-116">Remarks</span></span>

<span data-ttu-id="acbcc-117">Um verbo é uma cadeia de caracteres usada para especificar uma ação específica à qual um item dá suporte.</span><span class="sxs-lookup"><span data-stu-id="acbcc-117">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="acbcc-118">Normalmente, chamar um verbo inicia um aplicativo relacionado.</span><span class="sxs-lookup"><span data-stu-id="acbcc-118">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="acbcc-119">Por exemplo, chamar o verbo **Open** em um arquivo. txt normalmente abre o arquivo com um editor de texto, geralmente o bloco de notas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="acbcc-119">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="acbcc-120">O objeto [**FolderItemVerbs**](folderitemverbs.md) representa a coleção de verbos associados ao item.</span><span class="sxs-lookup"><span data-stu-id="acbcc-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="acbcc-121">Para obter mais informações sobre verbos, consulte [iniciando aplicativos](launch.md).</span><span class="sxs-lookup"><span data-stu-id="acbcc-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

<span data-ttu-id="acbcc-122">Esse método é semelhante a [**InvokeVerb**](folderitem-invokeverb.md), mas permite que você especifique argumentos para o comando, bem como o próprio comando.</span><span class="sxs-lookup"><span data-stu-id="acbcc-122">This method is similar to [**InvokeVerb**](folderitem-invokeverb.md), but it allows you to specify arguments to the command as well as the command itself.</span></span>

## <a name="examples"></a><span data-ttu-id="acbcc-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="acbcc-123">Examples</span></span>

<span data-ttu-id="acbcc-124">Os exemplos a seguir mostram o uso apropriado desse método no JScript, no VBScript e no Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="acbcc-124">The following examples show the proper use of this method in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="acbcc-125">JScript</span><span class="sxs-lookup"><span data-stu-id="acbcc-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
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
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



<span data-ttu-id="acbcc-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="acbcc-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
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
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="acbcc-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="acbcc-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
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
                    objFolderItem2.InvokeVerbEx ("open")
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



## <a name="requirements"></a><span data-ttu-id="acbcc-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acbcc-128">Requirements</span></span>



| <span data-ttu-id="acbcc-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="acbcc-129">Requirement</span></span> | <span data-ttu-id="acbcc-130">Valor</span><span class="sxs-lookup"><span data-stu-id="acbcc-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acbcc-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acbcc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="acbcc-132">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="acbcc-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="acbcc-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acbcc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="acbcc-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="acbcc-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="acbcc-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="acbcc-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="acbcc-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="acbcc-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="acbcc-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="acbcc-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="acbcc-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="acbcc-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="acbcc-139">DLL</span><span class="sxs-lookup"><span data-stu-id="acbcc-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acbcc-140"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="acbcc-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acbcc-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="acbcc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acbcc-142">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="acbcc-142">**ShellFolderItem**</span></span>](shellfolderitem-object.md)
</dt> <dt>

[<span data-ttu-id="acbcc-143">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="acbcc-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




