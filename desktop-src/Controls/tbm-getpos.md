---
title: Mensagem de TBM_GETPOS (commctrl. h)
description: Recupera a posição lógica atual do controle deslizante em um TrackBar. As posições lógicas são os valores inteiros no intervalo de TrackBar de mínimo para as posições do controle deslizante máximo.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- Controles de TBM_GETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ff9b8a107fe19afb1fee6107a2f05bad36025
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455176"
---
# <a name="tbm_getpos-message"></a><span data-ttu-id="965ab-105">\_Mensagem tbm GETPOS</span><span class="sxs-lookup"><span data-stu-id="965ab-105">TBM\_GETPOS message</span></span>

<span data-ttu-id="965ab-106">Recupera a posição lógica atual do controle deslizante em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="965ab-106">Retrieves the current logical position of the slider in a trackbar.</span></span> <span data-ttu-id="965ab-107">As posições lógicas são os valores inteiros no intervalo de TrackBar de mínimo para as posições do controle deslizante máximo.</span><span class="sxs-lookup"><span data-stu-id="965ab-107">The logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="965ab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="965ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="965ab-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="965ab-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="965ab-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="965ab-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="965ab-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="965ab-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="965ab-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="965ab-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="965ab-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="965ab-113">Return value</span></span>

<span data-ttu-id="965ab-114">Retorna um valor de 32 bits que especifica a posição lógica atual do controle deslizante do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="965ab-114">Returns a 32-bit value that specifies the current logical position of the trackbar's slider.</span></span>

## <a name="requirements"></a><span data-ttu-id="965ab-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="965ab-115">Requirements</span></span>



| <span data-ttu-id="965ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="965ab-116">Requirement</span></span> | <span data-ttu-id="965ab-117">Valor</span><span class="sxs-lookup"><span data-stu-id="965ab-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="965ab-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="965ab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="965ab-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="965ab-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="965ab-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="965ab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="965ab-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="965ab-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="965ab-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="965ab-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="965ab-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="965ab-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="965ab-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="965ab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="965ab-125">**TBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="965ab-125">**TBM\_SETPOS**</span></span>](tbm-setpos.md)
</dt> </dl>

 

 





