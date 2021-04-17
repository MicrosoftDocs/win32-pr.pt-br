---
title: WM_DSA_SHEET_CLOSE_NOTIFY mensagem
description: Postado no snap-in do Active Directory MMC quando uma folha de propriedades secundária é destruída.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_DSA_SHEET_CLOSE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f03cdb6224ae5f55bc995897d766ce61e67693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769119"
---
# <a name="wm_dsa_sheet_close_notify-message"></a><span data-ttu-id="b3897-104">\_Mensagem de \_ notificação de fechamento da folha do DSA do \_ WM \_</span><span class="sxs-lookup"><span data-stu-id="b3897-104">WM\_DSA\_SHEET\_CLOSE\_NOTIFY message</span></span>

<span data-ttu-id="b3897-105">A mensagem de **\_ notificação de \_ \_ fechamento \_ da folha DSA do WM** é postada no snap-in do Active Directory MMC quando uma folha de propriedades secundária é destruída.</span><span class="sxs-lookup"><span data-stu-id="b3897-105">The **WM\_DSA\_SHEET\_CLOSE\_NOTIFY** message is posted to the Active Directory MMC snap-in when a secondary property sheet is destroyed.</span></span>

> [!Note]  
> <span data-ttu-id="b3897-106">Esse valor de mensagem não está definido em um arquivo de cabeçalho publicado.</span><span class="sxs-lookup"><span data-stu-id="b3897-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="b3897-107">Para usar esse valor de mensagem, você mesmo deve defini-lo no formato exato mostrado.</span><span class="sxs-lookup"><span data-stu-id="b3897-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="b3897-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3897-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3897-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="b3897-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b3897-110">O identificador de janela da janela de snap-in que processará essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="b3897-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="b3897-111">Esse identificador é obtido do membro **hwndHidden** da estrutura [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="b3897-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3897-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3897-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3897-113">Contém um valor de 32 bits definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b3897-113">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="b3897-114">Isso é obtido do membro **wParamSheetClose** da estrutura [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="b3897-114">This is obtained from the **wParamSheetClose** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3897-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3897-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3897-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="b3897-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3897-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3897-117">Return value</span></span>

<span data-ttu-id="b3897-118">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="b3897-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3897-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3897-119">Requirements</span></span>



| <span data-ttu-id="b3897-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3897-120">Requirement</span></span> | <span data-ttu-id="b3897-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b3897-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b3897-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3897-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b3897-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3897-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b3897-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3897-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b3897-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3897-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3897-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3897-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3897-127">**PROPSHEETCFG**</span><span class="sxs-lookup"><span data-stu-id="b3897-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> </dl>

 

 





