---
title: Mensagem de HDM_HITTEST (commctrl. h)
description: Testa um ponto para determinar qual item de cabeçalho, se houver, está no ponto especificado.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- Controles de HDM_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085823"
---
# <a name="hdm_hittest-message"></a><span data-ttu-id="0cece-104">\_Mensagem HDM HITTEST</span><span class="sxs-lookup"><span data-stu-id="0cece-104">HDM\_HITTEST message</span></span>

<span data-ttu-id="0cece-105">Testa um ponto para determinar qual item de cabeçalho, se houver, está no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="0cece-105">Tests a point to determine which header item, if any, is at the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="0cece-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cece-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cece-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0cece-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0cece-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0cece-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0cece-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0cece-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cece-110">Um ponteiro para uma estrutura [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) que contém a posição para testar e receber informações sobre os resultados do teste.</span><span class="sxs-lookup"><span data-stu-id="0cece-110">A pointer to an [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) structure that contains the position to test and receives information about the results of the test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cece-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0cece-111">Return value</span></span>

<span data-ttu-id="0cece-112">Retorna o índice do item na posição especificada, se houver, ou 1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0cece-112">Returns the index of the item at the specified position, if any, or   1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cece-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cece-113">Requirements</span></span>



| <span data-ttu-id="0cece-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cece-114">Requirement</span></span> | <span data-ttu-id="0cece-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0cece-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cece-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cece-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0cece-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0cece-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0cece-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cece-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0cece-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0cece-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0cece-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0cece-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cece-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cece-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





