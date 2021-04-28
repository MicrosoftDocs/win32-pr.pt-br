---
description: Evento ShellFolderView. SelectionChanged – ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.
title: Evento ShellFolderView. SelectionChanged (shldisp. h)
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
ms.openlocfilehash: 31a32865a979bf6b5fa115912bdc32a9680e5064
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103994"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="b9eb4-103">Evento ShellFolderView. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="b9eb4-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="b9eb4-104">Ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.</span><span class="sxs-lookup"><span data-stu-id="b9eb4-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9eb4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9eb4-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="b9eb4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9eb4-106">Parameters</span></span>

<span data-ttu-id="b9eb4-107">Este manipulador de eventos não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b9eb4-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9eb4-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9eb4-108">Requirements</span></span>



| <span data-ttu-id="b9eb4-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9eb4-109">Requirement</span></span> | <span data-ttu-id="b9eb4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b9eb4-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9eb4-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9eb4-111">Minimum supported client</span></span><br/> | <span data-ttu-id="b9eb4-112">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b9eb4-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b9eb4-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9eb4-113">Minimum supported server</span></span><br/> | <span data-ttu-id="b9eb4-114">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b9eb4-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b9eb4-115">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b9eb4-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9eb4-116"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9eb4-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b9eb4-117">INSERI</span><span class="sxs-lookup"><span data-stu-id="b9eb4-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9eb4-118"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9eb4-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b9eb4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="b9eb4-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9eb4-120"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b9eb4-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




