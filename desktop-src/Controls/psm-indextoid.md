---
title: Mensagem de PSM_INDEXTOID (Prsht. h)
description: Obtém o índice de uma página de folha de propriedades e retorna sua ID de recurso. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet IndexToId.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- Controles de PSM_INDEXTOID de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009521"
---
# <a name="psm_indextoid-message"></a><span data-ttu-id="6af11-105">Mensagem de PSM \_ INDEXTOID</span><span class="sxs-lookup"><span data-stu-id="6af11-105">PSM\_INDEXTOID message</span></span>

<span data-ttu-id="6af11-106">Obtém o índice de uma página de folha de propriedades e retorna sua ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="6af11-106">Takes the index of a property sheet page and returns its resource ID.</span></span> <span data-ttu-id="6af11-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .</span><span class="sxs-lookup"><span data-stu-id="6af11-107">You can send this message explicitly or use the [**PropSheet\_IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6af11-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6af11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af11-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6af11-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6af11-110">Índice de base zero da página.</span><span class="sxs-lookup"><span data-stu-id="6af11-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="6af11-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6af11-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6af11-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6af11-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af11-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6af11-113">Return value</span></span>

<span data-ttu-id="6af11-114">Retorna a ID de recurso da página da folha de propriedades especificada por *wParam* , se bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6af11-114">Returns the resource ID of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="6af11-115">Caso contrário, retornará zero.</span><span class="sxs-lookup"><span data-stu-id="6af11-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6af11-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6af11-116">Requirements</span></span>



| <span data-ttu-id="6af11-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6af11-117">Requirement</span></span> | <span data-ttu-id="6af11-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6af11-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6af11-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6af11-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6af11-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6af11-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6af11-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6af11-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6af11-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6af11-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6af11-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6af11-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6af11-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="6af11-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





