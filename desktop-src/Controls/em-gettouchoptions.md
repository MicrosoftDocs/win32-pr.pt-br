---
title: Mensagem de EM_GETTOUCHOPTIONS (RichEdit. h)
description: Recupera as opções de toque associadas a um controle de edição rico.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- Controles de EM_GETTOUCHOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009607"
---
# <a name="em_gettouchoptions-message"></a><span data-ttu-id="af8e4-104">\_Mensagem em GETtouchoptions</span><span class="sxs-lookup"><span data-stu-id="af8e4-104">EM\_GETTOUCHOPTIONS message</span></span>

<span data-ttu-id="af8e4-105">Recupera as opções de toque associadas a um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="af8e4-105">Retrieves the touch options that are associated with a rich edit control.</span></span>


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a><span data-ttu-id="af8e4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af8e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af8e4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af8e4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af8e4-108">As opções de toque a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="af8e4-108">The touch options to retrieve.</span></span> <span data-ttu-id="af8e4-109">Pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="af8e4-109">It can be one of the following values.</span></span>



| <span data-ttu-id="af8e4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="af8e4-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="af8e4-111">Significado</span><span class="sxs-lookup"><span data-stu-id="af8e4-111">Meaning</span></span>                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="af8e4-112"><dt>**indisponibilidades de RTO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="af8e4-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="af8e4-113">Recupera se os garras de toque estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="af8e4-113">Retrieves whether the touch grippers are visible.</span></span><br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="af8e4-114"><dt>**\_DISABLEHANDLES RTO**</dt></span><span class="sxs-lookup"><span data-stu-id="af8e4-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="af8e4-115">A recuperação desse sinalizador não está implementada.</span><span class="sxs-lookup"><span data-stu-id="af8e4-115">Retrieving this flag is not implemented.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="af8e4-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af8e4-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af8e4-117">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="af8e4-117">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af8e4-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af8e4-118">Return value</span></span>

<span data-ttu-id="af8e4-119">Retorna o valor da opção especificada pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="af8e4-119">Returns the value of the option specified by the *wParam* parameter.</span></span> <span data-ttu-id="af8e4-120">Ele será diferente de zero se *wParam* for **RTO \_** e os garras de toque ficarão visíveis; zero, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="af8e4-120">It is nonzero if *wParam* is **RTO\_SHOWHANDLES** and the touch grippers are visible; zero, otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="af8e4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af8e4-121">Requirements</span></span>



| <span data-ttu-id="af8e4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="af8e4-122">Requirement</span></span> | <span data-ttu-id="af8e4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="af8e4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af8e4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af8e4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="af8e4-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="af8e4-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="af8e4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af8e4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="af8e4-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="af8e4-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af8e4-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af8e4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="af8e4-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="af8e4-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af8e4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="af8e4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af8e4-131">**em \_ SETtouchoptions**</span><span class="sxs-lookup"><span data-stu-id="af8e4-131">**EM\_SETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





