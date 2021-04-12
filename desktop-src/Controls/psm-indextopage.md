---
title: Mensagem de PSM_INDEXTOPAGE (Prsht. h)
description: Obtém o índice de uma página de folha de propriedades e retorna seu identificador HPROPSHEETPAGE. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet IndexToPage.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- Controles de PSM_INDEXTOPAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455654"
---
# <a name="psm_indextopage-message"></a><span data-ttu-id="b266d-105">Mensagem de PSM \_ INDEXTOPAGE</span><span class="sxs-lookup"><span data-stu-id="b266d-105">PSM\_INDEXTOPAGE message</span></span>

<span data-ttu-id="b266d-106">Obtém o índice de uma página de folha de propriedades e retorna seu identificador HPROPSHEETPAGE.</span><span class="sxs-lookup"><span data-stu-id="b266d-106">Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle.</span></span> <span data-ttu-id="b266d-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .</span><span class="sxs-lookup"><span data-stu-id="b266d-107">You can send this message explicitly or use the [**PropSheet\_IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b266d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b266d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b266d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b266d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b266d-110">Índice de base zero da página.</span><span class="sxs-lookup"><span data-stu-id="b266d-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="b266d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b266d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b266d-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b266d-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b266d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b266d-113">Return value</span></span>

<span data-ttu-id="b266d-114">Retorna o identificador HPROPSHEETPAGE da página da folha de propriedades especificada por *wParam* , se bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b266d-114">Returns the HPROPSHEETPAGE handle of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="b266d-115">Caso contrário, retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b266d-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b266d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b266d-116">Requirements</span></span>



| <span data-ttu-id="b266d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b266d-117">Requirement</span></span> | <span data-ttu-id="b266d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b266d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b266d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b266d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b266d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b266d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b266d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b266d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b266d-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b266d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b266d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b266d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b266d-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="b266d-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





