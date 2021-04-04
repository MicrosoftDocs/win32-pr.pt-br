---
title: Mensagem de TB_SETLISTGAP (commctrl. h)
description: Define a distância entre os botões da barra de ferramentas em uma barra de ferramentas específica.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- Controles de TB_SETLISTGAP de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824148"
---
# <a name="tb_setlistgap-message"></a><span data-ttu-id="74795-104">TB de \_ mensagem SETLISTGAP</span><span class="sxs-lookup"><span data-stu-id="74795-104">TB\_SETLISTGAP message</span></span>

<span data-ttu-id="74795-105">Define a distância entre os botões da barra de ferramentas em uma barra de ferramentas específica.</span><span class="sxs-lookup"><span data-stu-id="74795-105">Sets the distance between the toolbar buttons on a specific toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="74795-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74795-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74795-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74795-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74795-108">A lacuna, em pixels, entre os botões na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="74795-108">The gap, in pixels, between buttons on the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="74795-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74795-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74795-110">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="74795-110">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74795-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74795-111">Return value</span></span>

<span data-ttu-id="74795-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="74795-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74795-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="74795-113">Remarks</span></span>

<span data-ttu-id="74795-114">A lacuna entre os botões aplica-se apenas à janela de controle da barra de ferramentas que recebe essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="74795-114">The gap between buttons only applies to the toolbar control window that receives this message.</span></span> <span data-ttu-id="74795-115">O recebimento dessa mensagem dispara um redesenho da barra de ferramentas, se a barra de ferramentas estiver visível no momento.</span><span class="sxs-lookup"><span data-stu-id="74795-115">Receipt of this message triggers a repaint of the toolbar, if the toolbar is currently visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="74795-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74795-116">Requirements</span></span>



| <span data-ttu-id="74795-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="74795-117">Requirement</span></span> | <span data-ttu-id="74795-118">Valor</span><span class="sxs-lookup"><span data-stu-id="74795-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74795-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74795-119">Minimum supported client</span></span><br/> | <span data-ttu-id="74795-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74795-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74795-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74795-121">Minimum supported server</span></span><br/> | <span data-ttu-id="74795-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74795-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74795-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74795-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="74795-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74795-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





