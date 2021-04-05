---
title: WM_DSA_SHEET_CREATE_NOTIFY mensagem
description: Postado no snap-in do Active Directory MMC para criar uma folha de propriedades secundária.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_DSA_SHEET_CREATE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918527"
---
# <a name="wm_dsa_sheet_create_notify-message"></a><span data-ttu-id="880e2-104">\_Folha DSA do WM \_ \_ criar notificação de \_ mensagem</span><span class="sxs-lookup"><span data-stu-id="880e2-104">WM\_DSA\_SHEET\_CREATE\_NOTIFY message</span></span>

<span data-ttu-id="880e2-105">A mensagem de **\_ \_ \_ notificação criar \_ notificar do WM DSA sheet** é postada no snap-in Active Directory MMC para criar uma folha de propriedades secundária.</span><span class="sxs-lookup"><span data-stu-id="880e2-105">The **WM\_DSA\_SHEET\_CREATE\_NOTIFY** message is posted to the Active Directory MMC snap-in to create a secondary property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="880e2-106">Esse valor de mensagem não está definido em um arquivo de cabeçalho publicado.</span><span class="sxs-lookup"><span data-stu-id="880e2-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="880e2-107">Para usar esse valor de mensagem, defina-o no formato exato mostrado.</span><span class="sxs-lookup"><span data-stu-id="880e2-107">To use this message value, define it in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="880e2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="880e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="880e2-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="880e2-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="880e2-110">O identificador de janela da janela de snap-in que processará essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="880e2-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="880e2-111">Esse identificador é obtido do membro **hwndHidden** da estrutura [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="880e2-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="880e2-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="880e2-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="880e2-113">Contém um ponteiro para uma estrutura de [**\_ \_ \_ informações da página DSA s**](dsa-sec-page-info.md) que define a folha de propriedades secundária a ser criada.</span><span class="sxs-lookup"><span data-stu-id="880e2-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary property sheet to create.</span></span> <span data-ttu-id="880e2-114">O receptor da mensagem deve liberar essa memória com a função [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) quando ela não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="880e2-114">The message receiver must free this memory with the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function when it is no longer required.</span></span>

</dd> <dt>

<span data-ttu-id="880e2-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="880e2-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="880e2-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="880e2-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="880e2-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="880e2-117">Return value</span></span>

<span data-ttu-id="880e2-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="880e2-118">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="880e2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="880e2-119">Requirements</span></span>



| <span data-ttu-id="880e2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="880e2-120">Requirement</span></span> | <span data-ttu-id="880e2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="880e2-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="880e2-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="880e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="880e2-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="880e2-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="880e2-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="880e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="880e2-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="880e2-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="880e2-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="880e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="880e2-127">**PROPSHEETCFG**</span><span class="sxs-lookup"><span data-stu-id="880e2-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> <dt>

[<span data-ttu-id="880e2-128">**\_ \_ informações da página DSA SEC \_**</span><span class="sxs-lookup"><span data-stu-id="880e2-128">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="880e2-129">**LocalFree**</span><span class="sxs-lookup"><span data-stu-id="880e2-129">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

