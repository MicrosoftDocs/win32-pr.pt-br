---
title: Propriedade WebViewFolderContents.Folder (Shldisp.h)
description: Obtém um objeto Folder que representa a exibição.
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Propriedade da pasta recursos do ambiente herdado do Windows
- Propriedade da pasta recursos de ambiente herdados do Windows, objeto WebViewFolderContents
- Objeto WebViewFolderContents de recursos de ambiente do Windows herdados, propriedade da pasta
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0640d4e29b903b32a6c9ed1e0b1de9f458b132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454715"
---
# <a name="webviewfoldercontentsfolder-property"></a><span data-ttu-id="bfb5c-106">Propriedade WebViewFolderContents. Folder</span><span class="sxs-lookup"><span data-stu-id="bfb5c-106">WebViewFolderContents.Folder property</span></span>

<span data-ttu-id="bfb5c-107">Obtém um objeto [**Folder**](../shell/folder.md) que representa a exibição.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-107">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span>

<span data-ttu-id="bfb5c-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfb5c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfb5c-109">Syntax</span></span>


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a><span data-ttu-id="bfb5c-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bfb5c-110">Property value</span></span>

<span data-ttu-id="bfb5c-111">Um objeto que recebe o objeto de [**pasta**](../shell/folder.md) .</span><span class="sxs-lookup"><span data-stu-id="bfb5c-111">An object that receives the [**Folder**](../shell/folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="bfb5c-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bfb5c-112">Examples</span></span>

<span data-ttu-id="bfb5c-113">O exemplo a seguir mostra o uso apropriado dessa propriedade no JScript inserido em HTML.</span><span class="sxs-lookup"><span data-stu-id="bfb5c-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
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



## <a name="requirements"></a><span data-ttu-id="bfb5c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfb5c-114">Requirements</span></span>



| <span data-ttu-id="bfb5c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfb5c-115">Requirement</span></span> | <span data-ttu-id="bfb5c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bfb5c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb5c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfb5c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bfb5c-118">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bfb5c-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bfb5c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfb5c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bfb5c-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bfb5c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bfb5c-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bfb5c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfb5c-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfb5c-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bfb5c-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="bfb5c-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bfb5c-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bfb5c-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bfb5c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bfb5c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfb5c-126"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="bfb5c-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

