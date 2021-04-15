---
title: Mensagem de PSM_PAGETOINDEX (Prsht. h)
description: Usa o identificador HPROPSHEETPAGE da página da folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet PageToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- Controles de PSM_PAGETOINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753568"
---
# <a name="psm_pagetoindex-message"></a><span data-ttu-id="74bce-105">Mensagem de PSM \_ PAGETOINDEX</span><span class="sxs-lookup"><span data-stu-id="74bce-105">PSM\_PAGETOINDEX message</span></span>

<span data-ttu-id="74bce-106">Usa o identificador HPROPSHEETPAGE da página da folha de propriedades e retorna seu índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="74bce-106">Takes the HPROPSHEETPAGE handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="74bce-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .</span><span class="sxs-lookup"><span data-stu-id="74bce-107">You can send this message explicitly or use the [**PropSheet\_PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="74bce-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74bce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74bce-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74bce-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74bce-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="74bce-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="74bce-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74bce-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74bce-112">HPROPSHEETPAGE o identificador da página da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="74bce-112">HPROPSHEETPAGE handle to the property sheet page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74bce-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74bce-113">Return value</span></span>

<span data-ttu-id="74bce-114">Retorna o índice de base zero da página da folha de propriedades especificada por *lParam* , se obtiver êxito.</span><span class="sxs-lookup"><span data-stu-id="74bce-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="74bce-115">Caso contrário, ele retornará -1.</span><span class="sxs-lookup"><span data-stu-id="74bce-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="74bce-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74bce-116">Requirements</span></span>



| <span data-ttu-id="74bce-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="74bce-117">Requirement</span></span> | <span data-ttu-id="74bce-118">Valor</span><span class="sxs-lookup"><span data-stu-id="74bce-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="74bce-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74bce-119">Minimum supported client</span></span><br/> | <span data-ttu-id="74bce-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74bce-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="74bce-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74bce-121">Minimum supported server</span></span><br/> | <span data-ttu-id="74bce-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74bce-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="74bce-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74bce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="74bce-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="74bce-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





