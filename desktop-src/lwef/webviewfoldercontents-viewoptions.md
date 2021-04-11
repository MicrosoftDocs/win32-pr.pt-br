---
title: Propriedade WebViewFolderContents. ViewOptions (shldisp. h)
description: Obtém um conjunto de sinalizadores ShellFolderViewOptions que indicam as opções atuais da exibição.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Recursos de ambiente herdado do Windows da propriedade ViewOptions
- Propriedade ViewOptions recursos de ambiente herdados do Windows, objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, Propriedade ViewOptions
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008954"
---
# <a name="webviewfoldercontentsviewoptions-property"></a><span data-ttu-id="a8d73-106">Propriedade WebViewFolderContents. ViewOptions</span><span class="sxs-lookup"><span data-stu-id="a8d73-106">WebViewFolderContents.ViewOptions property</span></span>

<span data-ttu-id="a8d73-107">Obtém um conjunto de sinalizadores [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) que indicam as opções atuais da exibição.</span><span class="sxs-lookup"><span data-stu-id="a8d73-107">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span>

<span data-ttu-id="a8d73-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a8d73-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d73-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8d73-109">Syntax</span></span>


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="a8d73-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a8d73-110">Property value</span></span>

<span data-ttu-id="a8d73-111">Uma variável do tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de opções de exibição.</span><span class="sxs-lookup"><span data-stu-id="a8d73-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span>

## <a name="examples"></a><span data-ttu-id="a8d73-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a8d73-112">Examples</span></span>

<span data-ttu-id="a8d73-113">O exemplo a seguir mostra o uso apropriado dessa propriedade no JScript inserido em HTML.</span><span class="sxs-lookup"><span data-stu-id="a8d73-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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



## <a name="requirements"></a><span data-ttu-id="a8d73-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8d73-114">Requirements</span></span>



| <span data-ttu-id="a8d73-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8d73-115">Requirement</span></span> | <span data-ttu-id="a8d73-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a8d73-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d73-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8d73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d73-118">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a8d73-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a8d73-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8d73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d73-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a8d73-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8d73-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a8d73-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8d73-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8d73-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a8d73-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="a8d73-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8d73-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8d73-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a8d73-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a8d73-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8d73-126"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a8d73-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

