---
description: Método ShellFolderView.SelectItem – define o estado de seleção de um item na exibição.
title: Método ShellFolderView.SelectItem (Shldisp.h)
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
ms.openlocfilehash: ab0f65094f638c56df6a10434f9a404072278c55
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842547"
---
# <a name="shellfolderviewselectitem-method"></a><span data-ttu-id="a5497-103">Método ShellFolderView.SelectItem</span><span class="sxs-lookup"><span data-stu-id="a5497-103">ShellFolderView.SelectItem method</span></span>

<span data-ttu-id="a5497-104">Define o estado de seleção de um item na exibição.</span><span class="sxs-lookup"><span data-stu-id="a5497-104">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5497-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5497-105">Syntax</span></span>


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="a5497-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5497-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5497-107">*vItem* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="a5497-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5497-108">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="a5497-108">Type: **Variant\***</span></span>

<span data-ttu-id="a5497-109">O [**objeto FolderItem**](folderitem.md) para o qual o estado de seleção será definido.</span><span class="sxs-lookup"><span data-stu-id="a5497-109">The [**FolderItem**](folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="a5497-110">*dwFlags* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="a5497-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5497-111">Tipo: **Inteiro**</span><span class="sxs-lookup"><span data-stu-id="a5497-111">Type: **Integer**</span></span>

<span data-ttu-id="a5497-112">Um conjunto de sinalizadores que indicam o novo estado de seleção.</span><span class="sxs-lookup"><span data-stu-id="a5497-112">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="a5497-113">Pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5497-113">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="a5497-114"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="a5497-114">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a5497-115">Desmarque o item.</span><span class="sxs-lookup"><span data-stu-id="a5497-115">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="a5497-116">(1)</span><span class="sxs-lookup"><span data-stu-id="a5497-116">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a5497-117">Selecione o item.</span><span class="sxs-lookup"><span data-stu-id="a5497-117">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="a5497-118">(3)</span><span class="sxs-lookup"><span data-stu-id="a5497-118">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a5497-119">Coloque o item no modo de edição.</span><span class="sxs-lookup"><span data-stu-id="a5497-119">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="a5497-120">(4)</span><span class="sxs-lookup"><span data-stu-id="a5497-120">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a5497-121">Desmarque todos, menos o item especificado.</span><span class="sxs-lookup"><span data-stu-id="a5497-121">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="a5497-122">(8)</span><span class="sxs-lookup"><span data-stu-id="a5497-122">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a5497-123">Verifique se o item é exibido na exibição.</span><span class="sxs-lookup"><span data-stu-id="a5497-123">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="a5497-124">(16)</span><span class="sxs-lookup"><span data-stu-id="a5497-124">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a5497-125">Dê ao item o foco.</span><span class="sxs-lookup"><span data-stu-id="a5497-125">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5497-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5497-126">Return value</span></span>

<span data-ttu-id="a5497-127">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a5497-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5497-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5497-128">Remarks</span></span>

<span data-ttu-id="a5497-129">[**FocusedItem**](shellfolderview-focuseditem.md) só pode ser chamado no sistema local.</span><span class="sxs-lookup"><span data-stu-id="a5497-129">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="a5497-130">Ele não funcionará quando executado em uma página da Web por HTTP ou UNC.</span><span class="sxs-lookup"><span data-stu-id="a5497-130">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="a5497-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a5497-131">Examples</span></span>

<span data-ttu-id="a5497-132">O exemplo a seguir mostra o uso adequado desse método em JScript inserido em HTML.</span><span class="sxs-lookup"><span data-stu-id="a5497-132">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a5497-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5497-133">Requirements</span></span>



| <span data-ttu-id="a5497-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5497-134">Requirement</span></span> | <span data-ttu-id="a5497-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a5497-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5497-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5497-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a5497-137">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a5497-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a5497-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5497-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a5497-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a5497-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a5497-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a5497-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5497-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5497-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a5497-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="a5497-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5497-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5497-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a5497-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a5497-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5497-145"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a5497-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




