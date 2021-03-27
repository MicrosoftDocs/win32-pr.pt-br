---
description: 'Notifica o objeto de retorno de chamada que a barra de status está sendo atualizada. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_UPDATESTATUSBAR (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989016"
---
# <a name="sfvm_updatestatusbar-message"></a><span data-ttu-id="74c4b-104">\_Mensagem SFVM UPDATESTATUSBAR</span><span class="sxs-lookup"><span data-stu-id="74c4b-104">SFVM\_UPDATESTATUSBAR message</span></span>

<span data-ttu-id="74c4b-105">Notifica o objeto de retorno de chamada que a barra de status está sendo atualizada.</span><span class="sxs-lookup"><span data-stu-id="74c4b-105">Notifies the callback object that the status bar is being updated.</span></span> <span data-ttu-id="74c4b-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="74c4b-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a><span data-ttu-id="74c4b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74c4b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c4b-108">*fInitialize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74c4b-108">*fInitialize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c4b-109">Um valor **bool** que será definido como **true** se a barra de status estiver sendo inicializada.</span><span class="sxs-lookup"><span data-stu-id="74c4b-109">A **BOOL** value that is set to **TRUE** if the status bar is being initialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74c4b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="74c4b-110">Remarks</span></span>

<span data-ttu-id="74c4b-111">Quando você receber esta notificação:</span><span class="sxs-lookup"><span data-stu-id="74c4b-111">When you receive this notification:</span></span>

-   <span data-ttu-id="74c4b-112">Retorne \_ os S ok se você for manipular a atualização.</span><span class="sxs-lookup"><span data-stu-id="74c4b-112">Return S\_OK if you will handle the update.</span></span>
-   <span data-ttu-id="74c4b-113">Retorne MAKE \_ HRESULT ( \_ êxito de severidade, 0, 1) para que o objeto de exibição da pasta do sistema defina o texto da barra de status.</span><span class="sxs-lookup"><span data-stu-id="74c4b-113">Return MAKE\_HRESULT(SEVERITY\_SUCCESS,0,1) to have the system folder view object set the status bar text.</span></span>
-   <span data-ttu-id="74c4b-114">Return E \_ falha ao fazer com que o objeto de exibição da pasta do sistema manipule a barra de status.</span><span class="sxs-lookup"><span data-stu-id="74c4b-114">Return E\_FAIL to have the system folder view object handle the status bar.</span></span>

<span data-ttu-id="74c4b-115">O texto da barra de status padrão é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="74c4b-115">The default status bar text is as follows.</span></span>



| <span data-ttu-id="74c4b-116">Status</span><span class="sxs-lookup"><span data-stu-id="74c4b-116">Status</span></span>                      | <span data-ttu-id="74c4b-117">Texto da barra de status</span><span class="sxs-lookup"><span data-stu-id="74c4b-117">Status bar text</span></span>                         |
|-----------------------------|-----------------------------------------|
| <span data-ttu-id="74c4b-118">Nenhum item selecionado</span><span class="sxs-lookup"><span data-stu-id="74c4b-118">No items selected</span></span>           | <span data-ttu-id="74c4b-119">" \# \# Objects" (na pasta)</span><span class="sxs-lookup"><span data-stu-id="74c4b-119">"\#\# objects" (in the folder)</span></span>          |
| <span data-ttu-id="74c4b-120">Um item selecionado</span><span class="sxs-lookup"><span data-stu-id="74c4b-120">One item selected</span></span>           | <span data-ttu-id="74c4b-121">O InfoTip do item, se disponível.</span><span class="sxs-lookup"><span data-stu-id="74c4b-121">The infotip for the item, if available.</span></span> |
| <span data-ttu-id="74c4b-122">Mais de um item selecionado</span><span class="sxs-lookup"><span data-stu-id="74c4b-122">More than one item selected</span></span> | <span data-ttu-id="74c4b-123">" \# \# objetos selecionados"</span><span class="sxs-lookup"><span data-stu-id="74c4b-123">"\#\# objects selected"</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="74c4b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74c4b-124">Requirements</span></span>



| <span data-ttu-id="74c4b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="74c4b-125">Requirement</span></span> | <span data-ttu-id="74c4b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="74c4b-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74c4b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74c4b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="74c4b-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="74c4b-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="74c4b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74c4b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="74c4b-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="74c4b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74c4b-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="74c4b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="74c4b-132"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="74c4b-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
