---
title: Mensagem de TB_GETBUTTON (commctrl. h)
description: Recupera informações sobre o botão especificado em uma barra de ferramentas.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- Controles de TB_GETBUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2080a6c984bb2384f68a1388bd46fe598f5087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645265"
---
# <a name="tb_getbutton-message"></a><span data-ttu-id="fa9b3-104">Mensagem de $ BUTTON de TB \_</span><span class="sxs-lookup"><span data-stu-id="fa9b3-104">TB\_GETBUTTON message</span></span>

<span data-ttu-id="fa9b3-105">Recupera informações sobre o botão especificado em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-105">Retrieves information about the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa9b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa9b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa9b3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa9b3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9b3-108">Índice de base zero do botão para o qual recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="fa9b3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa9b3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9b3-110">Ponteiro para a estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que recebe as informações do botão.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-110">Pointer to the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that receives the button information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa9b3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa9b3-111">Return value</span></span>

<span data-ttu-id="fa9b3-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa9b3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa9b3-113">Requirements</span></span>



| <span data-ttu-id="fa9b3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa9b3-114">Requirement</span></span> | <span data-ttu-id="fa9b3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fa9b3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa9b3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa9b3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fa9b3-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa9b3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa9b3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa9b3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fa9b3-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa9b3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa9b3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa9b3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa9b3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa9b3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





