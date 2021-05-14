---
description: Evento ShellFolderView.SelectionChanged – ocorre quando o estado de seleção de qualquer item ou itens na exibição foi alterado.
title: Evento ShellFolderView.SelectionChanged (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: e91b72fd-fd26-4e38-8e80-41febec3ca03
ms.openlocfilehash: f029ffb217249909e966b592280abf38b2ba2edd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842567"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="733eb-103">Evento ShellFolderView.SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="733eb-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="733eb-104">Ocorre quando o estado de seleção de qualquer item ou item na exibição foi alterado.</span><span class="sxs-lookup"><span data-stu-id="733eb-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="733eb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="733eb-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="733eb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="733eb-106">Parameters</span></span>

<span data-ttu-id="733eb-107">Esse manipulador de eventos não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="733eb-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="733eb-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="733eb-108">Requirements</span></span>



| <span data-ttu-id="733eb-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="733eb-109">Requirement</span></span> | <span data-ttu-id="733eb-110">Valor</span><span class="sxs-lookup"><span data-stu-id="733eb-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="733eb-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="733eb-111">Minimum supported client</span></span><br/> | <span data-ttu-id="733eb-112">Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="733eb-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="733eb-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="733eb-113">Minimum supported server</span></span><br/> | <span data-ttu-id="733eb-114">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="733eb-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="733eb-115">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="733eb-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="733eb-116"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="733eb-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="733eb-117">Idl</span><span class="sxs-lookup"><span data-stu-id="733eb-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="733eb-118"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="733eb-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="733eb-119">DLL</span><span class="sxs-lookup"><span data-stu-id="733eb-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="733eb-120"><dt>Shell32.dll (versão 4.71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="733eb-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




