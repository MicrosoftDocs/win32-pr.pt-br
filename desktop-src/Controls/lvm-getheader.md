---
title: Mensagem de LVM_GETHEADER (commctrl. h)
description: Obtém o identificador para o controle de cabeçalho usado pelo controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetHeader de ListView.
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- Controles de LVM_GETHEADER de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETHEADER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d53082092118cad373005743849498791f0e1ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008936"
---
# <a name="lvm_getheader-message"></a><span data-ttu-id="7fae3-105">Mensagem do LVM \_ GETheader</span><span class="sxs-lookup"><span data-stu-id="7fae3-105">LVM\_GETHEADER message</span></span>

<span data-ttu-id="7fae3-106">Obtém o identificador para o controle de cabeçalho usado pelo controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="7fae3-106">Gets the handle to the header control used by the list-view control.</span></span> <span data-ttu-id="7fae3-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetHeader de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) .</span><span class="sxs-lookup"><span data-stu-id="7fae3-107">You can send this message explicitly or use the [**ListView\_GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7fae3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fae3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fae3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fae3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7fae3-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7fae3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7fae3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fae3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7fae3-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7fae3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fae3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7fae3-113">Return value</span></span>

<span data-ttu-id="7fae3-114">Retorna o identificador para o controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="7fae3-114">Returns the handle to the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fae3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fae3-115">Requirements</span></span>



| <span data-ttu-id="7fae3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fae3-116">Requirement</span></span> | <span data-ttu-id="7fae3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7fae3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fae3-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fae3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7fae3-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7fae3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fae3-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fae3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7fae3-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7fae3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fae3-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7fae3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fae3-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fae3-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





