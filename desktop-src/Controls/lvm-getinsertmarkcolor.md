---
title: Mensagem de LVM_GETINSERTMARKCOLOR (commctrl. h)
description: Recupera a cor do ponto de inserção.
ms.assetid: 1e98023a-9d26-4b87-bee4-bee4939ccfca
keywords:
- Controles de LVM_GETINSERTMARKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18d6e9ed277f447f5097c0954819029d24b9cbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086555"
---
# <a name="lvm_getinsertmarkcolor-message"></a><span data-ttu-id="c2e80-104">\_Mensagem GETINSERTMARKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="c2e80-104">LVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="c2e80-105">Recupera a cor do ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="c2e80-105">Retrieves the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2e80-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2e80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e80-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2e80-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c2e80-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c2e80-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c2e80-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2e80-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c2e80-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c2e80-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e80-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2e80-111">Return value</span></span>

<span data-ttu-id="c2e80-112">Retorna uma estrutura **COLORREF** que contém a cor do ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="c2e80-112">Returns a **COLORREF** structure that contains the color of the insertion point.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2e80-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2e80-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c2e80-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="c2e80-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c2e80-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c2e80-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2e80-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2e80-116">Requirements</span></span>



| <span data-ttu-id="c2e80-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e80-117">Requirement</span></span> | <span data-ttu-id="c2e80-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c2e80-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e80-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2e80-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e80-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2e80-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2e80-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2e80-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e80-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2e80-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2e80-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2e80-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2e80-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2e80-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





