---
title: Mensagem de TB_ISBUTTONPRESSED (commctrl. h)
description: Determina se o botão especificado em uma barra de ferramentas é pressionado.
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- Controles de TB_ISBUTTONPRESSED de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc2e6ec7b56ce205f3d89bc22a7c9dbbee90b1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085336"
---
# <a name="tb_isbuttonpressed-message"></a><span data-ttu-id="9d95d-104">TB de \_ mensagem ISBUTTONPRESSED</span><span class="sxs-lookup"><span data-stu-id="9d95d-104">TB\_ISBUTTONPRESSED message</span></span>

<span data-ttu-id="9d95d-105">Determina se o botão especificado em uma barra de ferramentas é pressionado.</span><span class="sxs-lookup"><span data-stu-id="9d95d-105">Determines whether the specified button in a toolbar is pressed.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d95d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d95d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d95d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d95d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d95d-108">Identificador de comando do botão.</span><span class="sxs-lookup"><span data-stu-id="9d95d-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="9d95d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d95d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9d95d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9d95d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d95d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d95d-111">Return value</span></span>

<span data-ttu-id="9d95d-112">Retornará zero se o botão for pressionado ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9d95d-112">Returns nonzero if the button is pressed, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d95d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d95d-113">Requirements</span></span>



| <span data-ttu-id="9d95d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d95d-114">Requirement</span></span> | <span data-ttu-id="9d95d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9d95d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d95d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d95d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9d95d-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d95d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d95d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d95d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9d95d-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9d95d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d95d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d95d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d95d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d95d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





