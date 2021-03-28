---
description: Chamado em resposta à exibição da Web Barricade sendo Descartado pelo usuário.
ms.assetid: 170893b6-c947-45b1-b717-a93a0b083bda
title: Método Pasta2. DismissedWebViewBarricade (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.DismissedWebViewBarricade
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cdedc7292b0dd52ca903b944993e32df1ec2c3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091613"
---
# <a name="folder2dismissedwebviewbarricade-method"></a><span data-ttu-id="8401c-103">Método Pasta2. DismissedWebViewBarricade</span><span class="sxs-lookup"><span data-stu-id="8401c-103">Folder2.DismissedWebViewBarricade method</span></span>

<span data-ttu-id="8401c-104">Chamado em resposta à exibição da Web Barricade sendo Descartado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8401c-104">Called in response to the web view barricade being dismissed by the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="8401c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8401c-105">Syntax</span></span>


```JScript
Folder2.DismissedWebViewBarricade()
```



## <a name="parameters"></a><span data-ttu-id="8401c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8401c-106">Parameters</span></span>

<span data-ttu-id="8401c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8401c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8401c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8401c-108">Return value</span></span>

<span data-ttu-id="8401c-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8401c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8401c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8401c-110">Remarks</span></span>

<span data-ttu-id="8401c-111">Um aplicativo chama esse método depois que o usuário ignora a exibição da Web Barricade.</span><span class="sxs-lookup"><span data-stu-id="8401c-111">An application calls this method after the user dismisses the web view barricade.</span></span>

## <a name="examples"></a><span data-ttu-id="8401c-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8401c-112">Examples</span></span>

<span data-ttu-id="8401c-113">O exemplo a seguir usa **DismissedWebViewBarricade** para especificar que a Barricade de exibição da Web para a pasta C: \\ Windows foi ignorada.</span><span class="sxs-lookup"><span data-stu-id="8401c-113">The following example uses **DismissedWebViewBarricade** to specify that the web view barricade for the C:\\Windows folder has been dismissed.</span></span> <span data-ttu-id="8401c-114">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8401c-114">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8401c-115">JScript</span><span class="sxs-lookup"><span data-stu-id="8401c-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectDismissedWebViewBarricadeJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            objFolder2.DismissedWebViewBarricade();
        }
    }
</script>
```



<span data-ttu-id="8401c-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="8401c-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectDismissedWebViewBarricadeVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            objFolder2.DismissedWebViewBarricade()
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="8401c-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8401c-117">Visual Basic:</span></span>


```VB
Private Sub btnDismissedWebViewBarricade_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.DismissedWebViewBarricade
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8401c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8401c-118">Requirements</span></span>



| <span data-ttu-id="8401c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8401c-119">Requirement</span></span> | <span data-ttu-id="8401c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8401c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8401c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8401c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8401c-122">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8401c-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8401c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8401c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8401c-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8401c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8401c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8401c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8401c-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8401c-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8401c-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="8401c-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8401c-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8401c-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8401c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8401c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8401c-130"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8401c-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8401c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8401c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8401c-132">**Pasta2**</span><span class="sxs-lookup"><span data-stu-id="8401c-132">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="8401c-133">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="8401c-133">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




