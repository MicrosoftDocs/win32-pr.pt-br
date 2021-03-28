---
description: Executa um verbo no item.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: Método FolderItem. InvokeVerb (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 259ff9613756940d5da8a37585dbf39fb2dc0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501157"
---
# <a name="folderiteminvokeverb-method"></a><span data-ttu-id="f9dae-103">Método FolderItem. InvokeVerb</span><span class="sxs-lookup"><span data-stu-id="f9dae-103">FolderItem.InvokeVerb method</span></span>

<span data-ttu-id="f9dae-104">Executa um verbo no item.</span><span class="sxs-lookup"><span data-stu-id="f9dae-104">Executes a verb on the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9dae-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9dae-105">Syntax</span></span>


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a><span data-ttu-id="f9dae-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9dae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9dae-107">*vVerb* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f9dae-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f9dae-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="f9dae-108">Type: **Variant**</span></span>

<span data-ttu-id="f9dae-109">Uma cadeia de caracteres que especifica o verbo a ser executado.</span><span class="sxs-lookup"><span data-stu-id="f9dae-109">A string that specifies the verb to be executed.</span></span> <span data-ttu-id="f9dae-110">Deve ser um dos valores retornados pela propriedade [**FolderItemVerb.Name**](folderitemverb-name.md) do item.</span><span class="sxs-lookup"><span data-stu-id="f9dae-110">It must be one of the values returned by the item's [**FolderItemVerb.Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="f9dae-111">Se nenhum verbo for especificado, o verbo padrão será invocado.</span><span class="sxs-lookup"><span data-stu-id="f9dae-111">If no verb is specified, the default verb will be invoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9dae-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9dae-112">Return value</span></span>

<span data-ttu-id="f9dae-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f9dae-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9dae-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9dae-114">Remarks</span></span>

<span data-ttu-id="f9dae-115">Um verbo é uma cadeia de caracteres usada para especificar uma ação específica à qual um item dá suporte.</span><span class="sxs-lookup"><span data-stu-id="f9dae-115">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="f9dae-116">Invocar um verbo é equivalente a selecionar um comando no menu de atalho de um item.</span><span class="sxs-lookup"><span data-stu-id="f9dae-116">Invoking a verb is equivalent to selecting a command from an item's shortcut menu.</span></span> <span data-ttu-id="f9dae-117">Normalmente, invocar um verbo inicia um aplicativo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f9dae-117">Typically, invoking a verb launches a related application.</span></span> <span data-ttu-id="f9dae-118">Por exemplo, invocar o verbo "Open" em um arquivo. txt abre o arquivo com um editor de texto, geralmente o bloco de notas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f9dae-118">For example, invoking the "open" verb on a .txt file opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="f9dae-119">Consulte [iniciando aplicativos](launch.md) para uma discussão adicional sobre verbos.</span><span class="sxs-lookup"><span data-stu-id="f9dae-119">See [Launching Applications](launch.md) for further discussion of verbs.</span></span>

<span data-ttu-id="f9dae-120">O objeto [**FolderItemVerbs**](folderitemverbs.md) representa a coleção de verbos associados ao item.</span><span class="sxs-lookup"><span data-stu-id="f9dae-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="f9dae-121">O verbo padrão pode variar para itens diferentes, mas normalmente é "aberto".</span><span class="sxs-lookup"><span data-stu-id="f9dae-121">The default verb may vary for different items, but it is typically "open".</span></span>

## <a name="examples"></a><span data-ttu-id="f9dae-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9dae-122">Examples</span></span>

<span data-ttu-id="f9dae-123">O exemplo a seguir usa **InvokeVerb** para invocar o verbo padrão ("Open" nesse caso) na pasta do Windows.</span><span class="sxs-lookup"><span data-stu-id="f9dae-123">The following example uses **InvokeVerb** to invoke the default verb ("open" in this case) on the Windows folder.</span></span> <span data-ttu-id="f9dae-124">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f9dae-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f9dae-125">JScript</span><span class="sxs-lookup"><span data-stu-id="f9dae-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



<span data-ttu-id="f9dae-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="f9dae-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
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
                                
                    objFolderItem.InvokeVerb()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="f9dae-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f9dae-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f9dae-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9dae-128">Requirements</span></span>



| <span data-ttu-id="f9dae-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9dae-129">Requirement</span></span> | <span data-ttu-id="f9dae-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f9dae-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9dae-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9dae-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f9dae-132">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f9dae-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f9dae-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9dae-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f9dae-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f9dae-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f9dae-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f9dae-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9dae-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9dae-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f9dae-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="f9dae-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9dae-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9dae-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f9dae-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f9dae-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9dae-140"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f9dae-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9dae-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9dae-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9dae-142">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="f9dae-142">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="f9dae-143">**Verbos**</span><span class="sxs-lookup"><span data-stu-id="f9dae-143">**Verbs**</span></span>](folderitem-verbs.md)
</dt> <dt>

[<span data-ttu-id="f9dae-144">**DoIt**</span><span class="sxs-lookup"><span data-stu-id="f9dae-144">**DoIt**</span></span>](folderitemverb-doit.md)
</dt> </dl>

 

 




