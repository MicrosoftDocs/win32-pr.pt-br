---
title: Mensagem de PSM_INDEXTOHWND (Prsht. h)
description: Usa o índice de uma página de folha de propriedades e retorna seu identificador de janela. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet IndexToHwnd.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- Controles de PSM_INDEXTOHWND de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086083"
---
# <a name="psm_indextohwnd-message"></a><span data-ttu-id="ae0e3-105">Mensagem de PSM \_ INDEXTOHWND</span><span class="sxs-lookup"><span data-stu-id="ae0e3-105">PSM\_INDEXTOHWND message</span></span>

<span data-ttu-id="ae0e3-106">Usa o índice de uma página de folha de propriedades e retorna seu identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="ae0e3-106">Takes the index of a property sheet page and returns its window handle.</span></span> <span data-ttu-id="ae0e3-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) .</span><span class="sxs-lookup"><span data-stu-id="ae0e3-107">You can send this message explicitly or use the [**PropSheet\_IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae0e3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae0e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae0e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae0e3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae0e3-110">Índice de base zero da página.</span><span class="sxs-lookup"><span data-stu-id="ae0e3-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="ae0e3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae0e3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae0e3-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ae0e3-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae0e3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae0e3-113">Return value</span></span>

<span data-ttu-id="ae0e3-114">Retorna o identificador para a janela da página da folha de propriedades especificada por *wParam* , se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ae0e3-114">Returns the handle to the window of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="ae0e3-115">Caso contrário, retornará zero.</span><span class="sxs-lookup"><span data-stu-id="ae0e3-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae0e3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae0e3-116">Requirements</span></span>



| <span data-ttu-id="ae0e3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae0e3-117">Requirement</span></span> | <span data-ttu-id="ae0e3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ae0e3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae0e3-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae0e3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae0e3-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae0e3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ae0e3-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae0e3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae0e3-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae0e3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ae0e3-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae0e3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae0e3-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae0e3-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





