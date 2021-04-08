---
title: Mensagem de TB_SETEXTENDEDSTYLE (commctrl. h)
description: Define os estilos estendidos para um controle ToolBar.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- Controles de TB_SETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086009"
---
# <a name="tb_setextendedstyle-message"></a><span data-ttu-id="67a4e-104">Mensagem de TB \_ SETextendedattribute</span><span class="sxs-lookup"><span data-stu-id="67a4e-104">TB\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="67a4e-105">Define os estilos estendidos para um controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="67a4e-105">Sets the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="67a4e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67a4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67a4e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67a4e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="67a4e-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="67a4e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="67a4e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67a4e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67a4e-110">Valor que especifica os novos estilos estendidos.</span><span class="sxs-lookup"><span data-stu-id="67a4e-110">Value specifying the new extended styles.</span></span> <span data-ttu-id="67a4e-111">Esse parâmetro pode ser uma combinação de [estilos estendidos](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="67a4e-111">This parameter can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67a4e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67a4e-112">Return value</span></span>

<span data-ttu-id="67a4e-113">Retorna um **DWORD** que representa os estilos estendidos anteriores.</span><span class="sxs-lookup"><span data-stu-id="67a4e-113">Returns a **DWORD** that represents the previous extended styles.</span></span> <span data-ttu-id="67a4e-114">Esse valor pode ser uma combinação de [estilos estendidos](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="67a4e-114">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67a4e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67a4e-115">Requirements</span></span>



| <span data-ttu-id="67a4e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="67a4e-116">Requirement</span></span> | <span data-ttu-id="67a4e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="67a4e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67a4e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67a4e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67a4e-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67a4e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67a4e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67a4e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67a4e-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="67a4e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67a4e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67a4e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="67a4e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="67a4e-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67a4e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="67a4e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a4e-125">**TB \_ Extended**</span><span class="sxs-lookup"><span data-stu-id="67a4e-125">**TB\_GETEXTENDEDSTYLE**</span></span>](tb-getextendedstyle.md)
</dt> </dl>

 

 





