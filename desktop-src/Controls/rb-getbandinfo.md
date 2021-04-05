---
title: Mensagem de RB_GETBANDINFO (commctrl. h)
description: Recupera informações sobre uma faixa especificada em um controle rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- Controles de RB_GETBANDINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085926"
---
# <a name="rb_getbandinfo-message"></a><span data-ttu-id="dbe4d-104">\_Mensagem GETBANDINFO RB</span><span class="sxs-lookup"><span data-stu-id="dbe4d-104">RB\_GETBANDINFO message</span></span>

<span data-ttu-id="dbe4d-105">Recupera informações sobre uma faixa especificada em um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="dbe4d-105">Retrieves information about a specified band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dbe4d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbe4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbe4d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dbe4d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe4d-108">Índice de base zero da banda para a qual as informações serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="dbe4d-108">Zero-based index of the band for which the information will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="dbe4d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbe4d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe4d-110">Ponteiro para uma estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que receberá as informações de banda solicitadas.</span><span class="sxs-lookup"><span data-stu-id="dbe4d-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that will receive the requested band information.</span></span> <span data-ttu-id="dbe4d-111">Antes de enviar essa mensagem, você deve definir o membro **cbSize** dessa estrutura como o tamanho da estrutura **REBARBANDINFO** e definir o membro **fMask** para os itens que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="dbe4d-111">Before sending this message, you must set the **cbSize** member of this structure to the size of the **REBARBANDINFO** structure and set the **fMask** member to the items you want to retrieve.</span></span> <span data-ttu-id="dbe4d-112">Além disso, você deve definir o membro **cch** da estrutura **REBARBANDINFO** para o tamanho do buffer **lpText** quando o \_ texto RBBIM for especificado.</span><span class="sxs-lookup"><span data-stu-id="dbe4d-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbe4d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dbe4d-113">Return value</span></span>

<span data-ttu-id="dbe4d-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="dbe4d-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe4d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbe4d-115">Requirements</span></span>



| <span data-ttu-id="dbe4d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbe4d-116">Requirement</span></span> | <span data-ttu-id="dbe4d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dbe4d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe4d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbe4d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe4d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbe4d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dbe4d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbe4d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe4d-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dbe4d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dbe4d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbe4d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbe4d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe4d-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="dbe4d-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="dbe4d-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dbe4d-125">**RB \_ GETBANDINFOW** (Unicode) e **RB \_ GETBANDINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dbe4d-125">**RB\_GETBANDINFOW** (Unicode) and **RB\_GETBANDINFOA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="dbe4d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbe4d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe4d-127">**\_SETBANDINFO RB**</span><span class="sxs-lookup"><span data-stu-id="dbe4d-127">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





