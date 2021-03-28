---
description: Obtém um objeto FolderItem que representa o item que tem o foco de entrada.
ms.assetid: ca88801d-c8fa-4c1c-9294-f52eada40ff6
title: Propriedade ShellFolderView. FocusedItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.FocusedItem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 26f0f24cddd3b9299ec70b41160579659c71b5bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171185"
---
# <a name="shellfolderviewfocuseditem-property"></a><span data-ttu-id="f4ca5-103">Propriedade ShellFolderView. FocusedItem</span><span class="sxs-lookup"><span data-stu-id="f4ca5-103">ShellFolderView.FocusedItem property</span></span>

<span data-ttu-id="f4ca5-104">Obtém um objeto [**FolderItem**](folderitem.md) que representa o item que tem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="f4ca5-104">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="f4ca5-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f4ca5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ca5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4ca5-106">Syntax</span></span>


```JScript
objFocusedItem = ShellFolderView.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="f4ca5-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f4ca5-107">Property value</span></span>

<span data-ttu-id="f4ca5-108">Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de item focado.</span><span class="sxs-lookup"><span data-stu-id="f4ca5-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ca5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4ca5-109">Remarks</span></span>

<span data-ttu-id="f4ca5-110">**FocusedItem** só pode ser chamado no sistema local.</span><span class="sxs-lookup"><span data-stu-id="f4ca5-110">**FocusedItem** can only be called on the local system.</span></span> <span data-ttu-id="f4ca5-111">Ele não funcionará quando for executado em uma página da Web por HTTP ou UNC.</span><span class="sxs-lookup"><span data-stu-id="f4ca5-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="f4ca5-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f4ca5-112">Examples</span></span>

<span data-ttu-id="f4ca5-113">O exemplo a seguir mostra o uso apropriado desse método no JScript inserido em HTML.</span><span class="sxs-lookup"><span data-stu-id="f4ca5-113">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFocusedItemJ()
    {
        var objFolderItem;
        
        objFolderItem = WebOC.Document.FocusedItem;
        if (objFolderItem != null)
        {
            alert("Got FolderItem object.");
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
<INPUT id=FocusedItem 
       type=button 
       value=FocusedItem 
       name=FocusedItem 
       onclick="fnShellFolderViewFocusedItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="f4ca5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4ca5-114">Requirements</span></span>



| <span data-ttu-id="f4ca5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4ca5-115">Requirement</span></span> | <span data-ttu-id="f4ca5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f4ca5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ca5-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4ca5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ca5-118">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f4ca5-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f4ca5-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4ca5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ca5-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f4ca5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f4ca5-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f4ca5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4ca5-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4ca5-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f4ca5-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="f4ca5-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f4ca5-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4ca5-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f4ca5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f4ca5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4ca5-126"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f4ca5-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
