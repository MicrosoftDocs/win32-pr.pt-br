---
title: Mensagem de TB_ISBUTTONCHECKED (commctrl. h)
description: Determina se o botão especificado em uma barra de ferramentas está marcado.
ms.assetid: ce576951-8db6-4854-8457-211ece018ce8
keywords:
- Controles de TB_ISBUTTONCHECKED de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONCHECKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb9bc573478ea55ce8e0bda48ff16679b135fc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499312"
---
# <a name="tb_isbuttonchecked-message"></a><span data-ttu-id="ef26a-104">TB de \_ mensagem ISBUTTONCHECKED</span><span class="sxs-lookup"><span data-stu-id="ef26a-104">TB\_ISBUTTONCHECKED message</span></span>

<span data-ttu-id="ef26a-105">Determina se o botão especificado em uma barra de ferramentas está marcado.</span><span class="sxs-lookup"><span data-stu-id="ef26a-105">Determines whether the specified button in a toolbar is checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef26a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef26a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef26a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef26a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef26a-108">Identificador de comando do botão.</span><span class="sxs-lookup"><span data-stu-id="ef26a-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="ef26a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef26a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ef26a-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ef26a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef26a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ef26a-111">Return value</span></span>

<span data-ttu-id="ef26a-112">Retornará zero se o botão estiver marcado, caso contrário, zero.</span><span class="sxs-lookup"><span data-stu-id="ef26a-112">Returns nonzero if the button is checked, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef26a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef26a-113">Requirements</span></span>



| <span data-ttu-id="ef26a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef26a-114">Requirement</span></span> | <span data-ttu-id="ef26a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ef26a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef26a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef26a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef26a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef26a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef26a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef26a-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef26a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef26a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef26a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





