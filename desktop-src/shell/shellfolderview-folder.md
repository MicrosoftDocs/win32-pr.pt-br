---
description: Obtém um objeto Folder que representa a exibição.
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: Propriedade ShellFolderView. Folder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 40590064048ba5410dc9341791aec443f16d68e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171183"
---
# <a name="shellfolderviewfolder-property"></a><span data-ttu-id="e1c45-103">Propriedade ShellFolderView. Folder</span><span class="sxs-lookup"><span data-stu-id="e1c45-103">ShellFolderView.Folder property</span></span>

<span data-ttu-id="e1c45-104">Obtém um objeto [**Folder**](folder.md) que representa a exibição.</span><span class="sxs-lookup"><span data-stu-id="e1c45-104">Gets a [**Folder**](folder.md) object that represents the view.</span></span>

<span data-ttu-id="e1c45-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e1c45-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1c45-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1c45-106">Syntax</span></span>


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a><span data-ttu-id="e1c45-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e1c45-107">Property value</span></span>

<span data-ttu-id="e1c45-108">Objeto que recebe o objeto de [**pasta**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="e1c45-108">Object that receives the [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1c45-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1c45-109">Remarks</span></span>

<span data-ttu-id="e1c45-110">A **pasta** só pode ser chamada no sistema local.</span><span class="sxs-lookup"><span data-stu-id="e1c45-110">**Folder** can only be called on the local system.</span></span> <span data-ttu-id="e1c45-111">Ele não funcionará quando for executado em uma página da Web por HTTP ou UNC.</span><span class="sxs-lookup"><span data-stu-id="e1c45-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="e1c45-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e1c45-112">Examples</span></span>

<span data-ttu-id="e1c45-113">O exemplo a seguir mostra o uso apropriado dessa propriedade para JScript Embedded em HTML.</span><span class="sxs-lookup"><span data-stu-id="e1c45-113">The following example shows the proper usage of this property for JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
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
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="e1c45-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1c45-114">Requirements</span></span>



| <span data-ttu-id="e1c45-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1c45-115">Requirement</span></span> | <span data-ttu-id="e1c45-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e1c45-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c45-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1c45-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e1c45-118">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e1c45-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e1c45-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1c45-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e1c45-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1c45-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e1c45-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e1c45-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1c45-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1c45-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e1c45-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="e1c45-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1c45-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1c45-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e1c45-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e1c45-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1c45-126"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e1c45-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




