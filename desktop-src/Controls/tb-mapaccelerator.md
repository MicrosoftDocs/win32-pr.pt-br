---
title: Mensagem de TB_MAPACCELERATOR (commctrl. h)
description: Determina a ID do botão que corresponde ao caractere de acelerador especificado.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- Controles de TB_MAPACCELERATOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644939"
---
# <a name="tb_mapaccelerator-message"></a><span data-ttu-id="4f761-104">TB de \_ mensagem MAPACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="4f761-104">TB\_MAPACCELERATOR message</span></span>

<span data-ttu-id="4f761-105">Determina a ID do botão que corresponde ao caractere de acelerador especificado.</span><span class="sxs-lookup"><span data-stu-id="4f761-105">Determines the ID of the button that corresponds to the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f761-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f761-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f761-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f761-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f761-108">O caractere do acelerador.</span><span class="sxs-lookup"><span data-stu-id="4f761-108">The accelerator character.</span></span>

</dd> <dt>

<span data-ttu-id="4f761-109">*lParam* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4f761-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f761-110">Ponteiro para um **uint**.</span><span class="sxs-lookup"><span data-stu-id="4f761-110">Pointer to a **UINT**.</span></span> <span data-ttu-id="4f761-111">No retorno, se for bem-sucedido, esse parâmetro manterá a ID do botão que tem *wParam* como seu caractere de acelerador.</span><span class="sxs-lookup"><span data-stu-id="4f761-111">On return, if successful, this parameter will hold the id of the button that has *wParam* as its accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f761-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f761-112">Return value</span></span>

<span data-ttu-id="4f761-113">Retorna um valor diferente de zero se um dos botões tiver *wParam* como seu caractere de acelerador, ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="4f761-113">Returns a nonzero value if one of the buttons has *wParam* as its accelerator character, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f761-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f761-114">Requirements</span></span>



| <span data-ttu-id="4f761-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f761-115">Requirement</span></span> | <span data-ttu-id="4f761-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4f761-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f761-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f761-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4f761-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f761-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f761-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f761-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4f761-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4f761-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f761-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f761-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f761-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f761-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4f761-123">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4f761-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4f761-124">**TB \_ MAPACCELERATORW** (Unicode) e **TB \_ MAPACCELERATORA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4f761-124">**TB\_MAPACCELERATORW** (Unicode) and **TB\_MAPACCELERATORA** (ANSI)</span></span><br/>       |



 

 





