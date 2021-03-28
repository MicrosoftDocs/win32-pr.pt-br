---
description: Obtém um objeto FolderItems que representa todos os itens selecionados na exibição.
title: Método ShellFolderView. SelectedItems (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectedItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1ee3bf2e-f9c9-47d9-a0f2-efedd69770c5
ms.openlocfilehash: c6ade3a6e25d5de6bfa1661207473dac72ace2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989063"
---
# <a name="shellfolderviewselecteditems-method"></a><span data-ttu-id="6c2bc-103">Método ShellFolderView. SelectedItems</span><span class="sxs-lookup"><span data-stu-id="6c2bc-103">ShellFolderView.SelectedItems method</span></span>

<span data-ttu-id="6c2bc-104">Obtém um objeto [**FolderItems**](folderitems.md) que representa todos os itens selecionados na exibição.</span><span class="sxs-lookup"><span data-stu-id="6c2bc-104">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c2bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c2bc-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="6c2bc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c2bc-106">Parameters</span></span>

<span data-ttu-id="6c2bc-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6c2bc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c2bc-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c2bc-108">Return value</span></span>

<span data-ttu-id="6c2bc-109">Tipo: **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6c2bc-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="6c2bc-110">Uma referência de objeto para o objeto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="6c2bc-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c2bc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c2bc-111">Remarks</span></span>

<span data-ttu-id="6c2bc-112">**SelectedItems** só pode ser chamado no sistema local.</span><span class="sxs-lookup"><span data-stu-id="6c2bc-112">**SelectedItems** can only be called on the local system.</span></span> <span data-ttu-id="6c2bc-113">Ele não funcionará quando for executado em uma página da Web por HTTP ou UNC.</span><span class="sxs-lookup"><span data-stu-id="6c2bc-113">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="6c2bc-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c2bc-114">Examples</span></span>

<span data-ttu-id="6c2bc-115">O exemplo a seguir mostra o uso apropriado desse método no JScript inserido em HTML.</span><span class="sxs-lookup"><span data-stu-id="6c2bc-115">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectedItemsJ()
    {
        var objFolderItems;
        
        objFolderItems = WebOC.Document.SelectedItems();
        if (objFolderItems != null)
        {
            alert("Got FolderItems object.");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC" 
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=SelectedItems 
       type=button 
       value=SelectedItems 
       name=SelectedItems 
       onclick="fnShellFolderViewSelectedItemsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="6c2bc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c2bc-116">Requirements</span></span>



| <span data-ttu-id="6c2bc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c2bc-117">Requirement</span></span> | <span data-ttu-id="6c2bc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6c2bc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c2bc-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c2bc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6c2bc-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6c2bc-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6c2bc-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c2bc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6c2bc-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6c2bc-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6c2bc-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6c2bc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c2bc-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c2bc-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6c2bc-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="6c2bc-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6c2bc-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6c2bc-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6c2bc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6c2bc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c2bc-128"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6c2bc-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




