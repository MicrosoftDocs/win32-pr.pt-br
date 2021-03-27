---
description: Executa um verbo em uma coleção de objetos FolderItem. Esse método é uma extensão do método InvokeVerb, permitindo um controle adicional da operação por meio de um conjunto de sinalizadores.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: Método FolderItems2. InvokeVerbEx (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aa9b986b5cb76f14cc950f522e1e289224c17b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967266"
---
# <a name="folderitems2invokeverbex-method"></a><span data-ttu-id="97292-104">Método FolderItems2. InvokeVerbEx</span><span class="sxs-lookup"><span data-stu-id="97292-104">FolderItems2.InvokeVerbEx method</span></span>

<span data-ttu-id="97292-105">Executa um verbo em uma coleção de objetos [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="97292-105">Executes a verb on a collection of [**FolderItem**](folderitem.md) objects.</span></span> <span data-ttu-id="97292-106">Esse método é uma extensão do método [**InvokeVerb**](folderitem-invokeverb.md) , permitindo um controle adicional da operação por meio de um conjunto de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="97292-106">This method is an extension of the [**InvokeVerb**](folderitem-invokeverb.md) method, allowing additional control of the operation through a set of flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="97292-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97292-107">Syntax</span></span>


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="97292-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97292-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97292-109">*vVerb* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="97292-109">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97292-110">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="97292-110">Type: **Variant**</span></span>

<span data-ttu-id="97292-111">Uma **variante** com a cadeia de caracteres de verbo que corresponde ao comando a ser executado.</span><span class="sxs-lookup"><span data-stu-id="97292-111">A **Variant** with the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="97292-112">Se nenhum verbo for especificado, o verbo padrão será executado.</span><span class="sxs-lookup"><span data-stu-id="97292-112">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="97292-113">*vArgs* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="97292-113">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97292-114">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="97292-114">Type: **Variant**</span></span>

<span data-ttu-id="97292-115">Uma **variante** que consiste em uma cadeia de caracteres com um ou mais argumentos para o comando especificado por *vVerb*.</span><span class="sxs-lookup"><span data-stu-id="97292-115">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="97292-116">O formato dessa cadeia de caracteres depende do verbo específico.</span><span class="sxs-lookup"><span data-stu-id="97292-116">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97292-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="97292-117">Remarks</span></span>

<span data-ttu-id="97292-118">Um verbo é uma cadeia de caracteres usada para especificar uma ação específica associada a um item ou a uma coleção de itens.</span><span class="sxs-lookup"><span data-stu-id="97292-118">A verb is a string used to specify a particular action associated with an item or collection of items.</span></span> <span data-ttu-id="97292-119">Normalmente, chamar um verbo inicia um aplicativo relacionado.</span><span class="sxs-lookup"><span data-stu-id="97292-119">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="97292-120">Por exemplo, chamar o verbo **Open** em um arquivo. txt normalmente abre o arquivo com um editor de texto, geralmente o bloco de notas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="97292-120">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="97292-121">Para obter mais informações sobre verbos, consulte [iniciando aplicativos](launch.md).</span><span class="sxs-lookup"><span data-stu-id="97292-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

## <a name="examples"></a><span data-ttu-id="97292-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97292-122">Examples</span></span>

<span data-ttu-id="97292-123">O exemplo a seguir usa **InvokeVerbEx** para invocar o verbo padrão ("Open") em **meu computador**.</span><span class="sxs-lookup"><span data-stu-id="97292-123">The following example uses **InvokeVerbEx** to invoke the default verb ("open") on **My Computer**.</span></span> <span data-ttu-id="97292-124">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="97292-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="97292-125">JScript</span><span class="sxs-lookup"><span data-stu-id="97292-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



<span data-ttu-id="97292-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="97292-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="97292-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="97292-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="97292-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97292-128">Requirements</span></span>



| <span data-ttu-id="97292-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="97292-129">Requirement</span></span> | <span data-ttu-id="97292-130">Valor</span><span class="sxs-lookup"><span data-stu-id="97292-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97292-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97292-131">Minimum supported client</span></span><br/> | <span data-ttu-id="97292-132">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="97292-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97292-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97292-133">Minimum supported server</span></span><br/> | <span data-ttu-id="97292-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97292-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="97292-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97292-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="97292-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="97292-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="97292-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="97292-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97292-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97292-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="97292-139">DLL</span><span class="sxs-lookup"><span data-stu-id="97292-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97292-140"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="97292-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97292-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="97292-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97292-142">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="97292-142">**FolderItems2**</span></span>](folderitems2-object.md)
</dt> <dt>

[<span data-ttu-id="97292-143">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="97292-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




