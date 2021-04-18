---
title: Propriedade WebViewFolderContents. script (shldisp. h)
description: Obtém o objeto de script para a exibição.
ms.assetid: f65246c5-3cd6-43bd-b267-ad27bdd0b41e
keywords:
- Recursos de ambiente do Windows herdados da propriedade script
- Propriedade script recursos de ambiente herdados do Windows, objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, Propriedade script
topic_type:
- apiref
api_name:
- WebViewFolderContents.Script
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92133278d73851fa43353c116a2385da9b0fd3da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810770"
---
# <a name="webviewfoldercontentsscript-property"></a><span data-ttu-id="9e2e0-106">Propriedade WebViewFolderContents. script</span><span class="sxs-lookup"><span data-stu-id="9e2e0-106">WebViewFolderContents.Script property</span></span>

<span data-ttu-id="9e2e0-107">Obtém o objeto de script para a exibição.</span><span class="sxs-lookup"><span data-stu-id="9e2e0-107">Gets the scripting object for the view.</span></span>

<span data-ttu-id="9e2e0-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9e2e0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e2e0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e2e0-109">Syntax</span></span>


```JScript
objScript = WebViewFolderContents.Script
```



## <a name="property-value"></a><span data-ttu-id="9e2e0-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e2e0-110">Property value</span></span>

<span data-ttu-id="9e2e0-111">Uma variável do tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de script.</span><span class="sxs-lookup"><span data-stu-id="9e2e0-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the scripting object.</span></span>

## <a name="examples"></a><span data-ttu-id="9e2e0-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9e2e0-112">Examples</span></span>

<span data-ttu-id="9e2e0-113">O exemplo a seguir mostra o uso apropriado dessa propriedade no JScript inserido em HTML.</span><span class="sxs-lookup"><span data-stu-id="9e2e0-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsScriptJ()
    {
        var objScript;

        objScript = FileList.Script;
        if (objScript != null)
        {
            alert(objScript.Name);
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



## <a name="requirements"></a><span data-ttu-id="9e2e0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e2e0-114">Requirements</span></span>



| <span data-ttu-id="9e2e0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e2e0-115">Requirement</span></span> | <span data-ttu-id="9e2e0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9e2e0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2e0-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e2e0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9e2e0-118">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9e2e0-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9e2e0-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e2e0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9e2e0-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e2e0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9e2e0-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9e2e0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e2e0-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e2e0-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9e2e0-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="9e2e0-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e2e0-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e2e0-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9e2e0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9e2e0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e2e0-126"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9e2e0-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

