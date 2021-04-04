---
title: Mensagem de TB_GETSTATE (commctrl. h)
description: Recupera informações sobre o estado do botão especificado em uma barra de ferramentas, como se ele está habilitado, pressionado ou marcado.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- Controles de TB_GETSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824245"
---
# <a name="tb_getstate-message"></a><span data-ttu-id="48a70-104">\_Mensagem de SETstate de TB</span><span class="sxs-lookup"><span data-stu-id="48a70-104">TB\_GETSTATE message</span></span>

<span data-ttu-id="48a70-105">Recupera informações sobre o estado do botão especificado em uma barra de ferramentas, como se ele está habilitado, pressionado ou marcado.</span><span class="sxs-lookup"><span data-stu-id="48a70-105">Retrieves information about the state of the specified button in a toolbar, such as whether it is enabled, pressed, or checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="48a70-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48a70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a70-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48a70-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48a70-108">Identificador de comando do botão para o qual recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="48a70-108">Command identifier of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="48a70-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48a70-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="48a70-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="48a70-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a70-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48a70-111">Return value</span></span>

<span data-ttu-id="48a70-112">Retorna as informações de estado do botão se for bem-sucedido ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="48a70-112">Returns the button state information if successful, or -1 otherwise.</span></span> <span data-ttu-id="48a70-113">As informações de estado do botão podem ser uma combinação dos valores listados em [**Estados de botão da barra de ferramentas**](toolbar-button-states.md).</span><span class="sxs-lookup"><span data-stu-id="48a70-113">The button state information can be a combination of the values listed in [**Toolbar Button States**](toolbar-button-states.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48a70-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48a70-114">Requirements</span></span>



| <span data-ttu-id="48a70-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a70-115">Requirement</span></span> | <span data-ttu-id="48a70-116">Valor</span><span class="sxs-lookup"><span data-stu-id="48a70-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48a70-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48a70-117">Minimum supported client</span></span><br/> | <span data-ttu-id="48a70-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48a70-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48a70-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48a70-119">Minimum supported server</span></span><br/> | <span data-ttu-id="48a70-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48a70-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48a70-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48a70-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="48a70-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="48a70-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





