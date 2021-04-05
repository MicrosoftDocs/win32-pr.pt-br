---
title: Mensagem de TB_ISBUTTONHIDDEN (commctrl. h)
description: Determina se o botão especificado em uma barra de ferramentas está oculto.
ms.assetid: 3372a64f-8209-4e3f-a6a9-8fe2e7e87ff2
keywords:
- Controles de TB_ISBUTTONHIDDEN de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIDDEN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db36f289a05fecfb2a0795965820324a9ce68057
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919229"
---
# <a name="tb_isbuttonhidden-message"></a><span data-ttu-id="22f74-104">TB de \_ mensagem ISBUTTONHIDDEN</span><span class="sxs-lookup"><span data-stu-id="22f74-104">TB\_ISBUTTONHIDDEN message</span></span>

<span data-ttu-id="22f74-105">Determina se o botão especificado em uma barra de ferramentas está oculto.</span><span class="sxs-lookup"><span data-stu-id="22f74-105">Determines whether the specified button in a toolbar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="22f74-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22f74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22f74-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22f74-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22f74-108">Identificador de comando do botão.</span><span class="sxs-lookup"><span data-stu-id="22f74-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="22f74-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22f74-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="22f74-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="22f74-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22f74-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22f74-111">Return value</span></span>

<span data-ttu-id="22f74-112">Retornará zero se o botão estiver oculto ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="22f74-112">Returns nonzero if the button is hidden, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="22f74-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22f74-113">Requirements</span></span>



| <span data-ttu-id="22f74-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="22f74-114">Requirement</span></span> | <span data-ttu-id="22f74-115">Valor</span><span class="sxs-lookup"><span data-stu-id="22f74-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22f74-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22f74-116">Minimum supported client</span></span><br/> | <span data-ttu-id="22f74-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22f74-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22f74-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22f74-118">Minimum supported server</span></span><br/> | <span data-ttu-id="22f74-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="22f74-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22f74-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22f74-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="22f74-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22f74-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





