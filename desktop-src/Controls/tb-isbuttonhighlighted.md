---
title: Mensagem de TB_ISBUTTONHIGHLIGHTED (commctrl. h)
description: Verifica o estado de realce de um botão da barra de ferramentas.
ms.assetid: d5aab670-a989-46f2-b4f8-d8a8968cbe07
keywords:
- Controles de TB_ISBUTTONHIGHLIGHTED de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIGHLIGHTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53e25058fee8fa5dcac218a641277ac46aed4e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009124"
---
# <a name="tb_isbuttonhighlighted-message"></a><span data-ttu-id="a9ddd-104">TB de \_ mensagem ISBUTTONHIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="a9ddd-104">TB\_ISBUTTONHIGHLIGHTED message</span></span>

<span data-ttu-id="a9ddd-105">Verifica o estado de realce de um botão da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a9ddd-105">Checks the highlight state of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9ddd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9ddd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9ddd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9ddd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ddd-108">Identificador de comando para um botão da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a9ddd-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="a9ddd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9ddd-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a9ddd-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a9ddd-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9ddd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9ddd-111">Return value</span></span>

<span data-ttu-id="a9ddd-112">Retornará um valor diferente de zero se o botão for realçado ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="a9ddd-112">Returns nonzero if the button is highlighted, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ddd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9ddd-113">Requirements</span></span>



| <span data-ttu-id="a9ddd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ddd-114">Requirement</span></span> | <span data-ttu-id="a9ddd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a9ddd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ddd-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9ddd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ddd-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9ddd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9ddd-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9ddd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ddd-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a9ddd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9ddd-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9ddd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9ddd-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9ddd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





