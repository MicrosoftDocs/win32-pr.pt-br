---
title: Mensagem de RB_MOVEBAND (commctrl. h)
description: Move uma banda de um índice para outro.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- Controles de RB_MOVEBAND de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454688"
---
# <a name="rb_moveband-message"></a><span data-ttu-id="ea263-104">\_Mensagem MOVEBAND RB</span><span class="sxs-lookup"><span data-stu-id="ea263-104">RB\_MOVEBAND message</span></span>

<span data-ttu-id="ea263-105">Move uma banda de um índice para outro.</span><span class="sxs-lookup"><span data-stu-id="ea263-105">Moves a band from one index to another.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea263-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea263-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea263-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea263-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea263-108">Índice de base zero da banda a ser movida.</span><span class="sxs-lookup"><span data-stu-id="ea263-108">Zero-based index of the band to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="ea263-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea263-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea263-110">Índice de base zero da nova posição de banda.</span><span class="sxs-lookup"><span data-stu-id="ea263-110">Zero-based index of the new band position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea263-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea263-111">Return value</span></span>

<span data-ttu-id="ea263-112">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="ea263-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea263-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea263-113">Remarks</span></span>

<span data-ttu-id="ea263-114">Provavelmente, essa mensagem alterará o índice de outras bandas no controle rebar.</span><span class="sxs-lookup"><span data-stu-id="ea263-114">This message will most likely change the index of other bands in the rebar control.</span></span> <span data-ttu-id="ea263-115">Se uma banda for movida do índice 6 para o índice 0, todas as faixas entre o terão seu índice incrementado em um.</span><span class="sxs-lookup"><span data-stu-id="ea263-115">If a band is moved from index 6 to index 0, all of the bands in between will have their index incremented by one.</span></span>

<span data-ttu-id="ea263-116">*lParam* nunca deve ser maior que o número de faixas menos um.</span><span class="sxs-lookup"><span data-stu-id="ea263-116">*lParam* must never be greater than the number of bands minus one.</span></span> <span data-ttu-id="ea263-117">O número de faixas pode ser obtido com a [**mensagem \_ GETBANDCOUNT RB**](rb-getbandcount.md) .</span><span class="sxs-lookup"><span data-stu-id="ea263-117">The number of bands can be obtained with the [**RB\_GETBANDCOUNT**](rb-getbandcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea263-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea263-118">Requirements</span></span>



| <span data-ttu-id="ea263-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea263-119">Requirement</span></span> | <span data-ttu-id="ea263-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ea263-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea263-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea263-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea263-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea263-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea263-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea263-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea263-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea263-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea263-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea263-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea263-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea263-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





