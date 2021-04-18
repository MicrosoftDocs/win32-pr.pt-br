---
title: Evento WebViewFolderContents. SelectionChanged (shldisp. h)
description: Ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- Recursos de ambiente herdado do Windows do evento SelectionChanged
topic_type:
- apiref
api_name:
- SelectionChanged
api_location:
- Shell32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8421e9d06ff9fd24256da8a23cdd100b5749968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499698"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a><span data-ttu-id="946df-104">Evento WebViewFolderContents. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="946df-104">WebViewFolderContents.SelectionChanged event</span></span>

<span data-ttu-id="946df-105">Ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.</span><span class="sxs-lookup"><span data-stu-id="946df-105">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="946df-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="946df-106">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="946df-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="946df-107">Parameters</span></span>

<span data-ttu-id="946df-108">Este manipulador de eventos não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="946df-108">This event handler has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="946df-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="946df-109">Examples</span></span>

<span data-ttu-id="946df-110">O exemplo a seguir mostra o uso apropriado desse evento para JScript Embedded em HTML.</span><span class="sxs-lookup"><span data-stu-id="946df-110">The following example shows the proper usage of this event for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectionChangedJ()
    {
        alert("SelectionChanged event was called");
    }
</script>

<script language="JavaScript" for="FileList" event="SelectionChanged">
    fnWebViewFolderContentsSelectionChangedJ();
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="946df-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="946df-111">Requirements</span></span>



| <span data-ttu-id="946df-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="946df-112">Requirement</span></span> | <span data-ttu-id="946df-113">Valor</span><span class="sxs-lookup"><span data-stu-id="946df-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="946df-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="946df-114">Minimum supported client</span></span><br/> | <span data-ttu-id="946df-115">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="946df-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="946df-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="946df-116">Minimum supported server</span></span><br/> | <span data-ttu-id="946df-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="946df-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="946df-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="946df-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="946df-119"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="946df-119"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="946df-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="946df-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="946df-121"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="946df-121"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="946df-122">DLL</span><span class="sxs-lookup"><span data-stu-id="946df-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="946df-123"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="946df-123"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





