---
description: Contém o status offline da pasta.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Propriedade Pasta2. OfflineStatus (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967280"
---
# <a name="folder2offlinestatus-property"></a><span data-ttu-id="6b87f-103">Propriedade Pasta2. OfflineStatus</span><span class="sxs-lookup"><span data-stu-id="6b87f-103">Folder2.OfflineStatus property</span></span>

<span data-ttu-id="6b87f-104">Contém o status offline da pasta.</span><span class="sxs-lookup"><span data-stu-id="6b87f-104">Contains the offline status of the folder.</span></span>

<span data-ttu-id="6b87f-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6b87f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b87f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b87f-106">Syntax</span></span>


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a><span data-ttu-id="6b87f-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6b87f-107">Property value</span></span>

<span data-ttu-id="6b87f-108">Um **inteiro** que é definido como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6b87f-108">An **Integer** that is set to one of the following values.</span></span>

<dt>



 <span data-ttu-id="6b87f-109">(OFS \_ DIRTYCACHE)</span><span class="sxs-lookup"><span data-stu-id="6b87f-109">(OFS\_DIRTYCACHE)</span></span>


</dt> <dd>

<span data-ttu-id="6b87f-110">O servidor está online com alterações não sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="6b87f-110">Server is online with unsynchronized changes.</span></span>

</dd> <dt>



 <span data-ttu-id="6b87f-111">(OFS \_ INATIVO</span><span class="sxs-lookup"><span data-stu-id="6b87f-111">(OFS\_INACTIVE)</span></span>


</dt> <dd>

<span data-ttu-id="6b87f-112">O cache offline não está habilitado para esta pasta.</span><span class="sxs-lookup"><span data-stu-id="6b87f-112">Offline caching is not enabled for this folder.</span></span>

</dd> <dt>



 <span data-ttu-id="6b87f-113">(OFS \_ ESTÁ</span><span class="sxs-lookup"><span data-stu-id="6b87f-113">(OFS\_OFFLINE)</span></span>


</dt> <dd>

<span data-ttu-id="6b87f-114">O servidor está offline.</span><span class="sxs-lookup"><span data-stu-id="6b87f-114">Server is offline.</span></span>

</dd> <dt>



 <span data-ttu-id="6b87f-115">(OFS \_ CONECTAR</span><span class="sxs-lookup"><span data-stu-id="6b87f-115">(OFS\_ONLINE)</span></span>


</dt> <dd>

<span data-ttu-id="6b87f-116">O servidor está online.</span><span class="sxs-lookup"><span data-stu-id="6b87f-116">Server is online.</span></span>

</dd> <dt>



 <span data-ttu-id="6b87f-117">(OFS \_ SERVERBACK)</span><span class="sxs-lookup"><span data-stu-id="6b87f-117">(OFS\_SERVERBACK)</span></span>


</dt> <dd>

<span data-ttu-id="6b87f-118">O servidor está offline, mas pode ser acessado.</span><span class="sxs-lookup"><span data-stu-id="6b87f-118">Server is offline but can be reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b87f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b87f-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6b87f-120">Arquivos Offline deve ser habilitado por meio de opções de pasta para que o **OfflineStatus** funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="6b87f-120">Offline Files must be enabled through Folder Options for **OfflineStatus** to work correctly.</span></span> <span data-ttu-id="6b87f-121">Se a opção Arquivos Offline não estiver habilitada, a propriedade retornará **OFS \_ inativa**.</span><span class="sxs-lookup"><span data-stu-id="6b87f-121">If the Offline Files option is not enabled, the property returns **OFS\_INACTIVE**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="6b87f-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b87f-122">Examples</span></span>

<span data-ttu-id="6b87f-123">O exemplo a seguir mostra o uso apropriado de **OfflineStatus** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6b87f-123">The following example shows the proper use of **OfflineStatus** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6b87f-124">JScript</span><span class="sxs-lookup"><span data-stu-id="6b87f-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



<span data-ttu-id="6b87f-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="6b87f-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="6b87f-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6b87f-126">Visual Basic:</span></span>


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6b87f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b87f-127">Requirements</span></span>



| <span data-ttu-id="6b87f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b87f-128">Requirement</span></span> | <span data-ttu-id="6b87f-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6b87f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b87f-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b87f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6b87f-131">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6b87f-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b87f-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b87f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6b87f-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b87f-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6b87f-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b87f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b87f-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b87f-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6b87f-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="6b87f-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b87f-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b87f-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6b87f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6b87f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b87f-139"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6b87f-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b87f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b87f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b87f-141">**Pasta2**</span><span class="sxs-lookup"><span data-stu-id="6b87f-141">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="6b87f-142">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="6b87f-142">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




