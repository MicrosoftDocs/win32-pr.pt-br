---
description: Indica que o estado de seleção de um ou mais itens na exibição foi alterado.
title: Evento ShellFolderViewOC. SelectionChanged (shldisp. h)
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
ms.assetid: 85c37f4e-229f-4383-8218-10f8c2b0b8a0
ms.openlocfilehash: 53d6fc3eb6f13d136af603a3129ba75a46c3c6a6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841037"
---
# <a name="shellfolderviewocselectionchanged-event"></a><span data-ttu-id="50a24-103">Evento ShellFolderViewOC. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="50a24-103">ShellFolderViewOC.SelectionChanged event</span></span>

<span data-ttu-id="50a24-104">Indica que o estado de seleção de um ou mais itens na exibição foi alterado.</span><span class="sxs-lookup"><span data-stu-id="50a24-104">Indicates that the selection state of one or more items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="50a24-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50a24-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="50a24-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50a24-106">Parameters</span></span>

<span data-ttu-id="50a24-107">Este manipulador de eventos não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="50a24-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="50a24-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="50a24-108">Remarks</span></span>

<span data-ttu-id="50a24-109">Forneça o código de manipulação de eventos para esse evento, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="50a24-109">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="50a24-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50a24-110">Requirements</span></span>



| <span data-ttu-id="50a24-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="50a24-111">Requirement</span></span> | <span data-ttu-id="50a24-112">Valor</span><span class="sxs-lookup"><span data-stu-id="50a24-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50a24-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50a24-113">Minimum supported client</span></span><br/> | <span data-ttu-id="50a24-114">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="50a24-114">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50a24-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50a24-115">Minimum supported server</span></span><br/> | <span data-ttu-id="50a24-116">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50a24-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="50a24-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50a24-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="50a24-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="50a24-118"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="50a24-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="50a24-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50a24-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50a24-120"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="50a24-121">DLL</span><span class="sxs-lookup"><span data-stu-id="50a24-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50a24-122"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="50a24-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50a24-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="50a24-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50a24-124">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="50a24-124">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




