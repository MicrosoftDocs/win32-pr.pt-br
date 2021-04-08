---
title: Mensagem de TB_INSERTMARKHITTEST (commctrl. h)
description: Recupera as informações de marca de inserção de um ponto em uma barra de ferramentas.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- Controles de TB_INSERTMARKHITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009192"
---
# <a name="tb_insertmarkhittest-message"></a><span data-ttu-id="5127c-104">TB de \_ mensagem INSERTMARKHITTEST</span><span class="sxs-lookup"><span data-stu-id="5127c-104">TB\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="5127c-105">Recupera as informações de marca de inserção de um ponto em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="5127c-105">Retrieves the insertion mark information for a point in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5127c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5127c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5127c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5127c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5127c-108">Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que contém as coordenadas de teste de clique, em relação à área do cliente da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="5127c-108">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the hit test coordinates, relative to the client area of the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="5127c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5127c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5127c-110">Ponteiro para uma estrutura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que recebe as informações de marca de inserção.</span><span class="sxs-lookup"><span data-stu-id="5127c-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5127c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5127c-111">Return value</span></span>

<span data-ttu-id="5127c-112">Retornará zero se o ponto for uma marca de inserção, ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="5127c-112">Returns nonzero if the point is an insertion mark, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5127c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5127c-113">Requirements</span></span>



| <span data-ttu-id="5127c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5127c-114">Requirement</span></span> | <span data-ttu-id="5127c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5127c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5127c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5127c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5127c-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5127c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5127c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5127c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5127c-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5127c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5127c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5127c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5127c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5127c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

