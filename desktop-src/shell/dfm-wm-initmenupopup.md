---
description: Enviado quando um menu suspenso ou submenu está prestes a ficar ativo. Isso permite que um aplicativo modifique o menu antes que ele seja exibido, sem alterar o menu inteiro.
title: Mensagem de DFM_WM_INITMENUPOPUP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1c89731bdffc0e7d902e6c83b9a4f208134b7cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090022"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="91769-104">Mensagem do DFM do \_ WM \_ INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="91769-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="91769-105">Enviado quando um menu suspenso ou submenu está prestes a ficar ativo.</span><span class="sxs-lookup"><span data-stu-id="91769-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="91769-106">Isso permite que um aplicativo modifique o menu antes que ele seja exibido, sem alterar o menu inteiro.</span><span class="sxs-lookup"><span data-stu-id="91769-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="91769-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91769-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91769-108">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91769-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91769-109">Um identificador para o menu suspenso ou submenu.</span><span class="sxs-lookup"><span data-stu-id="91769-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="91769-110">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91769-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91769-111">A palavra de ordem inferior Especifica a posição relativa de base zero do item de menu que abre o menu suspenso ou o submenu.</span><span class="sxs-lookup"><span data-stu-id="91769-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="91769-112">A palavra de ordem superior indica se o menu suspenso é o menu janela.</span><span class="sxs-lookup"><span data-stu-id="91769-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="91769-113">Se o menu for o menu janela, esse parâmetro será **true**; caso contrário, será **false**.</span><span class="sxs-lookup"><span data-stu-id="91769-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91769-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91769-114">Return value</span></span>

<span data-ttu-id="91769-115">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="91769-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="91769-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91769-116">Requirements</span></span>



| <span data-ttu-id="91769-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="91769-117">Requirement</span></span> | <span data-ttu-id="91769-118">Valor</span><span class="sxs-lookup"><span data-stu-id="91769-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="91769-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91769-119">Minimum supported client</span></span><br/> | <span data-ttu-id="91769-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91769-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="91769-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91769-121">Minimum supported server</span></span><br/> | <span data-ttu-id="91769-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="91769-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="91769-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91769-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="91769-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="91769-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




