---
description: Sincroniza todos os arquivos offline na pasta.
ms.assetid: b149df96-0c8e-47b9-b71e-2ad5dcfdeb8f
title: Método Pasta2. Synchronize (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Synchronize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e9c39c37ff0e44e58aa71c69496dec8bee2745bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370516"
---
# <a name="folder2synchronize-method"></a><span data-ttu-id="8ed6c-103">Método Pasta2. Synchronize</span><span class="sxs-lookup"><span data-stu-id="8ed6c-103">Folder2.Synchronize method</span></span>

<span data-ttu-id="8ed6c-104">Sincroniza todos os arquivos offline na pasta.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-104">Synchronizes all offline files in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed6c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ed6c-105">Syntax</span></span>


```JScript
iRetVal = Folder2.Synchronize()
```



## <a name="parameters"></a><span data-ttu-id="8ed6c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ed6c-106">Parameters</span></span>

<span data-ttu-id="8ed6c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ed6c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ed6c-108">Remarks</span></span>

<span data-ttu-id="8ed6c-109">Para usar esse método, o recurso Arquivos Offline deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-109">To use this method, the Offline Files feature must be enabled.</span></span>

## <a name="examples"></a><span data-ttu-id="8ed6c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8ed6c-110">Examples</span></span>

<span data-ttu-id="8ed6c-111">O exemplo a seguir mostra o uso apropriado de **Synchronize** for JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-111">The following example shows the proper use of **Synchronize** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8ed6c-112">JScript</span><span class="sxs-lookup"><span data-stu-id="8ed6c-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnSynchronizeJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            objFolder2.Synchronize();
        }
    }
</script>
```



<span data-ttu-id="8ed6c-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="8ed6c-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnSynchronizeVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            objFolder2.Synchronize
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="8ed6c-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8ed6c-114">Visual Basic:</span></span>


```VB
Private Sub fnSynchronizeVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.Synchronize
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8ed6c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ed6c-115">Requirements</span></span>



| <span data-ttu-id="8ed6c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ed6c-116">Requirement</span></span> | <span data-ttu-id="8ed6c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8ed6c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed6c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ed6c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8ed6c-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8ed6c-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ed6c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ed6c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8ed6c-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ed6c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8ed6c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ed6c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ed6c-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ed6c-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8ed6c-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="8ed6c-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ed6c-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ed6c-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8ed6c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8ed6c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ed6c-127"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8ed6c-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ed6c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ed6c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed6c-129">**Pasta2**</span><span class="sxs-lookup"><span data-stu-id="8ed6c-129">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="8ed6c-130">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="8ed6c-130">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




