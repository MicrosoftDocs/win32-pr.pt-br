---
title: Mensagem de TB_REPLACEBITMAP (commctrl. h)
description: Substitui um bitmap existente por um novo bitmap.
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- Controles de TB_REPLACEBITMAP de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0216d73f70f9bef8230d7e725834d63d60012798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824613"
---
# <a name="tb_replacebitmap-message"></a><span data-ttu-id="f7782-104">TB de \_ mensagem REPLACEBITMAP</span><span class="sxs-lookup"><span data-stu-id="f7782-104">TB\_REPLACEBITMAP message</span></span>

<span data-ttu-id="f7782-105">Substitui um bitmap existente por um novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="f7782-105">Replaces an existing bitmap with a new bitmap.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7782-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7782-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7782-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7782-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f7782-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f7782-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f7782-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7782-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7782-110">Ponteiro para uma estrutura [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) que contém as informações do bitmap a ser substituído e o novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="f7782-110">Pointer to a [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) structure that contains the information of the bitmap to be replaced and the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7782-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7782-111">Return value</span></span>

<span data-ttu-id="f7782-112">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="f7782-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7782-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7782-113">Requirements</span></span>



| <span data-ttu-id="f7782-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7782-114">Requirement</span></span> | <span data-ttu-id="f7782-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f7782-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7782-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7782-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f7782-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7782-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7782-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7782-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f7782-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f7782-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7782-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7782-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7782-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7782-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





