---
description: Define o estado de seleção de um item na exibição.
title: Método ShellFolderView. SelectItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: d44633983075cdf22581bce05cfb7c073f422084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171178"
---
# <a name="shellfolderviewselectitem-method"></a><span data-ttu-id="2a76e-103">Método ShellFolderView. SelectItem</span><span class="sxs-lookup"><span data-stu-id="2a76e-103">ShellFolderView.SelectItem method</span></span>

<span data-ttu-id="2a76e-104">Define o estado de seleção de um item na exibição.</span><span class="sxs-lookup"><span data-stu-id="2a76e-104">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a76e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a76e-105">Syntax</span></span>


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="2a76e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a76e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a76e-107">*vItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a76e-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a76e-108">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="2a76e-108">Type: \**Variant\** _</span></span>

<span data-ttu-id="2a76e-109">O objeto [_ *FolderItem* \*](folderitem.md) para o qual o estado de seleção será definido.</span><span class="sxs-lookup"><span data-stu-id="2a76e-109">The [_ *FolderItem*\*](folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="2a76e-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a76e-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a76e-111">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="2a76e-111">Type: **Integer**</span></span>

<span data-ttu-id="2a76e-112">Um conjunto de sinalizadores que indicam o novo estado de seleção.</span><span class="sxs-lookup"><span data-stu-id="2a76e-112">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="2a76e-113">Pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a76e-113">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="2a76e-114"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="2a76e-114">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2a76e-115">Desmarque o item.</span><span class="sxs-lookup"><span data-stu-id="2a76e-115">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="2a76e-116">(1)</span><span class="sxs-lookup"><span data-stu-id="2a76e-116">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2a76e-117">Selecione o item.</span><span class="sxs-lookup"><span data-stu-id="2a76e-117">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="2a76e-118">(3)</span><span class="sxs-lookup"><span data-stu-id="2a76e-118">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2a76e-119">Coloque o item no modo de edição.</span><span class="sxs-lookup"><span data-stu-id="2a76e-119">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="2a76e-120">(4)</span><span class="sxs-lookup"><span data-stu-id="2a76e-120">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2a76e-121">Anular seleção de todos, exceto o item especificado.</span><span class="sxs-lookup"><span data-stu-id="2a76e-121">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="2a76e-122">(8)</span><span class="sxs-lookup"><span data-stu-id="2a76e-122">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2a76e-123">Verifique se o item é exibido na exibição.</span><span class="sxs-lookup"><span data-stu-id="2a76e-123">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="2a76e-124">(16)</span><span class="sxs-lookup"><span data-stu-id="2a76e-124">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2a76e-125">Dê o foco ao item.</span><span class="sxs-lookup"><span data-stu-id="2a76e-125">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a76e-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a76e-126">Return value</span></span>

<span data-ttu-id="2a76e-127">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2a76e-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a76e-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a76e-128">Remarks</span></span>

<span data-ttu-id="2a76e-129">[**FocusedItem**](shellfolderview-focuseditem.md) só pode ser chamado no sistema local.</span><span class="sxs-lookup"><span data-stu-id="2a76e-129">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="2a76e-130">Ele não funcionará quando for executado em uma página da Web por HTTP ou UNC.</span><span class="sxs-lookup"><span data-stu-id="2a76e-130">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="2a76e-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2a76e-131">Examples</span></span>

<span data-ttu-id="2a76e-132">O exemplo a seguir mostra o uso apropriado desse método no JScript inserido em HTML.</span><span class="sxs-lookup"><span data-stu-id="2a76e-132">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
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
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="2a76e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a76e-133">Requirements</span></span>



| <span data-ttu-id="2a76e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a76e-134">Requirement</span></span> | <span data-ttu-id="2a76e-135">Valor</span><span class="sxs-lookup"><span data-stu-id="2a76e-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a76e-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a76e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2a76e-137">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2a76e-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2a76e-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a76e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2a76e-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2a76e-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2a76e-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2a76e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a76e-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a76e-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2a76e-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="2a76e-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a76e-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a76e-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2a76e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2a76e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a76e-145"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2a76e-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




