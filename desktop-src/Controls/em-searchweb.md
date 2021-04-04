---
title: Mensagem de EM_SEARCHWEB (commctrl. h)
description: Abre o navegador e executa uma pesquisa na Web com o texto selecionado como o termo de pesquisa.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Controles de EM_SEARCHWEB de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824643"
---
# <a name="em_searchweb-message"></a><span data-ttu-id="ed13f-104">\_Mensagem em SEARCHWEB</span><span class="sxs-lookup"><span data-stu-id="ed13f-104">EM\_SEARCHWEB message</span></span>

<span data-ttu-id="ed13f-105">Abre o navegador e executa uma pesquisa na Web com o texto selecionado como o termo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ed13f-105">Opens the browser and performs a web search with the selected text as the search term.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed13f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed13f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed13f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed13f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed13f-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ed13f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ed13f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed13f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed13f-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ed13f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed13f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed13f-111">Return value</span></span>

<span data-ttu-id="ed13f-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ed13f-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed13f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed13f-113">Remarks</span></span>

<span data-ttu-id="ed13f-114">Se o recurso "Pesquisar na Web" for desabilitado usando a mensagem em [**\_ ENABLESEARCHWEB**](em-enablesearchweb.md) , essa mensagem não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="ed13f-114">If the "Search the web" feature is disabled using the [**EM\_ENABLESEARCHWEB**](em-enablesearchweb.md) message, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed13f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed13f-115">Requirements</span></span>



| <span data-ttu-id="ed13f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed13f-116">Requirement</span></span> | <span data-ttu-id="ed13f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ed13f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed13f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed13f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ed13f-119">\[Somente aplicativos de área de trabalho do Windows 10, 1809\]</span><span class="sxs-lookup"><span data-stu-id="ed13f-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed13f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed13f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ed13f-121">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="ed13f-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed13f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed13f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed13f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed13f-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed13f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed13f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed13f-125">**em \_ ENABLESEARCHWEB**</span><span class="sxs-lookup"><span data-stu-id="ed13f-125">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> </dl>

 

 





