---
description: Ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.
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
ms.openlocfilehash: 864cd4c7bb0b414e4237c698412ad10899c8cbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011608"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="c659b-103">Evento ShellFolderView. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="c659b-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="c659b-104">Ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.</span><span class="sxs-lookup"><span data-stu-id="c659b-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c659b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c659b-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="c659b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c659b-106">Parameters</span></span>

<span data-ttu-id="c659b-107">Este manipulador de eventos não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c659b-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c659b-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c659b-108">Requirements</span></span>



| <span data-ttu-id="c659b-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="c659b-109">Requirement</span></span> | <span data-ttu-id="c659b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="c659b-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c659b-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c659b-111">Minimum supported client</span></span><br/> | <span data-ttu-id="c659b-112">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c659b-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c659b-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c659b-113">Minimum supported server</span></span><br/> | <span data-ttu-id="c659b-114">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c659b-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c659b-115">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c659b-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="c659b-116"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c659b-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c659b-117">INSERI</span><span class="sxs-lookup"><span data-stu-id="c659b-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c659b-118"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c659b-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c659b-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c659b-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c659b-120"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c659b-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




