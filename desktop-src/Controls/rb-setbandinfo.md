---
title: Mensagem de RB_SETBANDINFO (commctrl. h)
description: Define características de uma banda existente em um controle rebar.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- Controles de RB_SETBANDINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455529"
---
# <a name="rb_setbandinfo-message"></a><span data-ttu-id="859db-104">\_Mensagem SETBANDINFO RB</span><span class="sxs-lookup"><span data-stu-id="859db-104">RB\_SETBANDINFO message</span></span>

<span data-ttu-id="859db-105">Define características de uma banda existente em um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="859db-105">Sets characteristics of an existing band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="859db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="859db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="859db-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="859db-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="859db-108">Índice de base zero da banda para receber as novas configurações.</span><span class="sxs-lookup"><span data-stu-id="859db-108">Zero-based index of the band to receive the new settings.</span></span>

</dd> <dt>

<span data-ttu-id="859db-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="859db-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="859db-110">Ponteiro para uma estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que define a banda a ser modificada e as novas configurações.</span><span class="sxs-lookup"><span data-stu-id="859db-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be modified and the new settings.</span></span> <span data-ttu-id="859db-111">Antes de enviar essa mensagem, você deve definir o membro **cbSize** dessa estrutura como a estrutura **sizeof**(REBARBANDINFO).</span><span class="sxs-lookup"><span data-stu-id="859db-111">Before sending this message, you must set the **cbSize** member of this structure to the **sizeof**(REBARBANDINFO) structure.</span></span> <span data-ttu-id="859db-112">Além disso, você deve definir o membro **cch** da estrutura **REBARBANDINFO** para o tamanho do buffer **lpText** quando o \_ texto RBBIM for especificado.</span><span class="sxs-lookup"><span data-stu-id="859db-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="859db-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="859db-113">Return value</span></span>

<span data-ttu-id="859db-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="859db-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="859db-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="859db-115">Requirements</span></span>



| <span data-ttu-id="859db-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="859db-116">Requirement</span></span> | <span data-ttu-id="859db-117">Valor</span><span class="sxs-lookup"><span data-stu-id="859db-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="859db-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="859db-118">Minimum supported client</span></span><br/> | <span data-ttu-id="859db-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="859db-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="859db-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="859db-120">Minimum supported server</span></span><br/> | <span data-ttu-id="859db-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="859db-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="859db-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="859db-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="859db-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="859db-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="859db-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="859db-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="859db-125">**RB \_ SETBANDINFOW** (Unicode) e **RB \_ SETBANDINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="859db-125">**RB\_SETBANDINFOW** (Unicode) and **RB\_SETBANDINFOA** (ANSI)</span></span><br/>             |



 

 





