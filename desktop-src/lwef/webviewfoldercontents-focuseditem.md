---
title: Propriedade WebViewFolderContents. FocusedItem (shldisp. h)
description: Obtém um objeto FolderItem que representa o item que tem o foco de entrada.
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- Recursos do ambiente Windows herdado da propriedade FocusedItem
- Propriedade FocusedItem recursos de ambiente do Windows herdados, objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, Propriedade FocusedItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e7c2a4c280a949ec3684e2b05610830315a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369258"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a><span data-ttu-id="16688-106">Propriedade WebViewFolderContents. FocusedItem</span><span class="sxs-lookup"><span data-stu-id="16688-106">WebViewFolderContents.FocusedItem property</span></span>

<span data-ttu-id="16688-107">Obtém um objeto [**FolderItem**](../shell/folderitem.md) que representa o item que tem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="16688-107">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="16688-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="16688-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="16688-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16688-109">Syntax</span></span>


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="16688-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="16688-110">Property value</span></span>

<span data-ttu-id="16688-111">Uma variável do tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de item focado.</span><span class="sxs-lookup"><span data-stu-id="16688-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="examples"></a><span data-ttu-id="16688-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16688-112">Examples</span></span>

<span data-ttu-id="16688-113">O exemplo a seguir mostra o uso apropriado dessa propriedade no JScript inserido em HTML.</span><span class="sxs-lookup"><span data-stu-id="16688-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="16688-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16688-114">Requirements</span></span>



| <span data-ttu-id="16688-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="16688-115">Requirement</span></span> | <span data-ttu-id="16688-116">Valor</span><span class="sxs-lookup"><span data-stu-id="16688-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16688-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16688-117">Minimum supported client</span></span><br/> | <span data-ttu-id="16688-118">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="16688-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="16688-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16688-119">Minimum supported server</span></span><br/> | <span data-ttu-id="16688-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="16688-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="16688-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="16688-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="16688-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="16688-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="16688-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="16688-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="16688-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="16688-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="16688-125">DLL</span><span class="sxs-lookup"><span data-stu-id="16688-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16688-126"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="16688-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

