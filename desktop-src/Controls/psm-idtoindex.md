---
title: Mensagem de PSM_IDTOINDEX (Prsht. h)
description: Usa a ID de recurso de uma página de folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet IdToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- Controles de PSM_IDTOINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086087"
---
# <a name="psm_idtoindex-message"></a><span data-ttu-id="1ab22-105">Mensagem de PSM \_ IDTOINDEX</span><span class="sxs-lookup"><span data-stu-id="1ab22-105">PSM\_IDTOINDEX message</span></span>

<span data-ttu-id="1ab22-106">Usa a ID de recurso de uma página de folha de propriedades e retorna seu índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="1ab22-106">Takes the resource ID of a property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="1ab22-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) .</span><span class="sxs-lookup"><span data-stu-id="1ab22-107">You can send this message explicitly or use the [**PropSheet\_IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ab22-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ab22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ab22-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ab22-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ab22-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1ab22-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1ab22-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ab22-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ab22-112">ID de recurso da página.</span><span class="sxs-lookup"><span data-stu-id="1ab22-112">Resource ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ab22-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ab22-113">Return value</span></span>

<span data-ttu-id="1ab22-114">Retorna o índice de base zero da página da folha de propriedades especificada por *lParam* , se obtiver êxito.</span><span class="sxs-lookup"><span data-stu-id="1ab22-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="1ab22-115">Caso contrário, ele retornará -1.</span><span class="sxs-lookup"><span data-stu-id="1ab22-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ab22-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ab22-116">Requirements</span></span>



| <span data-ttu-id="1ab22-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ab22-117">Requirement</span></span> | <span data-ttu-id="1ab22-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1ab22-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab22-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ab22-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1ab22-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ab22-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1ab22-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ab22-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1ab22-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ab22-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1ab22-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ab22-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ab22-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ab22-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





