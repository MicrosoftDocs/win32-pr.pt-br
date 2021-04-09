---
title: Mensagem de PSM_HWNDTOINDEX (Prsht. h)
description: Usa o identificador de janela da página da folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet HwndToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- Controles de PSM_HWNDTOINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085728"
---
# <a name="psm_hwndtoindex-message"></a><span data-ttu-id="b6ea5-105">Mensagem de PSM \_ HWNDTOINDEX</span><span class="sxs-lookup"><span data-stu-id="b6ea5-105">PSM\_HWNDTOINDEX message</span></span>

<span data-ttu-id="b6ea5-106">Usa o identificador de janela da página da folha de propriedades e retorna seu índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-106">Takes the window handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="b6ea5-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) .</span><span class="sxs-lookup"><span data-stu-id="b6ea5-107">You can send this message explicitly or use the [**PropSheet\_HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6ea5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6ea5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ea5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6ea5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6ea5-110">Identificador para a janela da página.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-110">Handle to the page's window.</span></span>

</dd> <dt>

<span data-ttu-id="b6ea5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6ea5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6ea5-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6ea5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6ea5-113">Return value</span></span>

<span data-ttu-id="b6ea5-114">Retorna o índice de base zero da página da folha de propriedades especificada por *wParam* , se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-114">Returns the zero-based index of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="b6ea5-115">Caso contrário, ele retornará -1.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ea5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6ea5-116">Requirements</span></span>



| <span data-ttu-id="b6ea5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6ea5-117">Requirement</span></span> | <span data-ttu-id="b6ea5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b6ea5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ea5-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6ea5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ea5-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6ea5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b6ea5-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6ea5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ea5-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6ea5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b6ea5-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6ea5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6ea5-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6ea5-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





