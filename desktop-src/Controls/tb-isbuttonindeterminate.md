---
title: Mensagem de TB_ISBUTTONINDETERMINATE (commctrl. h)
description: Determina se o botão especificado em uma barra de ferramentas é indeterminado.
ms.assetid: b4d759b3-cdbc-417b-9da4-4ed9edc38c0e
keywords:
- Controles de TB_ISBUTTONINDETERMINATE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONINDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc024efcad9f0f48ae4882b019269903c249bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009123"
---
# <a name="tb_isbuttonindeterminate-message"></a><span data-ttu-id="62749-104">TB de \_ mensagem ISBUTTONINDETERMINATE</span><span class="sxs-lookup"><span data-stu-id="62749-104">TB\_ISBUTTONINDETERMINATE message</span></span>

<span data-ttu-id="62749-105">Determina se o botão especificado em uma barra de ferramentas é indeterminado.</span><span class="sxs-lookup"><span data-stu-id="62749-105">Determines whether the specified button in a toolbar is indeterminate.</span></span>

## <a name="parameters"></a><span data-ttu-id="62749-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62749-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62749-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62749-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62749-108">Identificador de comando do botão.</span><span class="sxs-lookup"><span data-stu-id="62749-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="62749-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62749-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="62749-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="62749-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62749-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62749-111">Return value</span></span>

<span data-ttu-id="62749-112">Retornará zero se o botão for indeterminado ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="62749-112">Returns nonzero if the button is indeterminate, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="62749-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62749-113">Requirements</span></span>



| <span data-ttu-id="62749-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="62749-114">Requirement</span></span> | <span data-ttu-id="62749-115">Valor</span><span class="sxs-lookup"><span data-stu-id="62749-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62749-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62749-116">Minimum supported client</span></span><br/> | <span data-ttu-id="62749-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62749-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62749-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62749-118">Minimum supported server</span></span><br/> | <span data-ttu-id="62749-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62749-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62749-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62749-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="62749-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62749-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





