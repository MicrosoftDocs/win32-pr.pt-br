---
title: Mensagem de TB_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera os estilos estendidos para um controle ToolBar.
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- Controles de TB_GETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80bc4f4ad45e5c1c75366e0890f3fd76ec1fa74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644577"
---
# <a name="tb_getextendedstyle-message"></a><span data-ttu-id="2b969-104">Mensagem de TB \_ Extended</span><span class="sxs-lookup"><span data-stu-id="2b969-104">TB\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="2b969-105">Recupera os estilos estendidos para um controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="2b969-105">Retrieves the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b969-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b969-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b969-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b969-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2b969-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2b969-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2b969-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b969-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2b969-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2b969-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b969-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b969-111">Return value</span></span>

<span data-ttu-id="2b969-112">Retorna um **DWORD** que representa os estilos atualmente em uso para o controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="2b969-112">Returns a **DWORD** that represents the styles currently in use for the toolbar control.</span></span> <span data-ttu-id="2b969-113">Esse valor pode ser uma combinação de [estilos estendidos](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="2b969-113">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b969-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b969-114">Requirements</span></span>



| <span data-ttu-id="2b969-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b969-115">Requirement</span></span> | <span data-ttu-id="2b969-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2b969-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b969-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b969-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2b969-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b969-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b969-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b969-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2b969-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2b969-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b969-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b969-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b969-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b969-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b969-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b969-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b969-124">**TB \_ SETextendedattribute**</span><span class="sxs-lookup"><span data-stu-id="2b969-124">**TB\_SETEXTENDEDSTYLE**</span></span>](tb-setextendedstyle.md)
</dt> </dl>

 

 





