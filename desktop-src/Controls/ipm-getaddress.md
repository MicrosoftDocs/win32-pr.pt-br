---
title: Mensagem de IPM_GETADDRESS (commctrl. h)
description: Obtém os valores de endereço para todos os quatro campos no controle de endereço IP.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- Controles de IPM_GETADDRESS de mensagens do Windows
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918705"
---
# <a name="ipm_getaddress-message"></a><span data-ttu-id="6502b-104">\_Mensagem de GETADDRESS IPM</span><span class="sxs-lookup"><span data-stu-id="6502b-104">IPM\_GETADDRESS message</span></span>

<span data-ttu-id="6502b-105">Obtém os valores de endereço para todos os quatro campos no controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="6502b-105">Gets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6502b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6502b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6502b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6502b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6502b-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6502b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6502b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6502b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6502b-110">Um ponteiro para um valor **DWORD** que recebe o endereço.</span><span class="sxs-lookup"><span data-stu-id="6502b-110">A pointer to a **DWORD** value that receives the address.</span></span> <span data-ttu-id="6502b-111">O valor do campo 3 estará contido em bits 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="6502b-111">The field 3 value will be contained in bits 0 through 7.</span></span> <span data-ttu-id="6502b-112">O valor do campo 2 estará contido em bits 8 a 15.</span><span class="sxs-lookup"><span data-stu-id="6502b-112">The field 2 value will be contained in bits 8 through 15.</span></span> <span data-ttu-id="6502b-113">O valor do campo 1 estará contido nos bits 16 a 23.</span><span class="sxs-lookup"><span data-stu-id="6502b-113">The field 1 value will be contained in bits 16 through 23.</span></span> <span data-ttu-id="6502b-114">O valor do campo 0 estará contido em bits 24 a 31.</span><span class="sxs-lookup"><span data-stu-id="6502b-114">The field 0 value will be contained in bits 24 through 31.</span></span> <span data-ttu-id="6502b-115">O [**primeiro \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), [**o \_ segundo**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress)IPAddress, o [**terceiro \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)e o [**quarto \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) macros também podem ser usados para extrair as informações de endereço.</span><span class="sxs-lookup"><span data-stu-id="6502b-115">The [**FIRST\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), [**SECOND\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**THIRD\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress), and [**FOURTH\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) macros can also be used to extract the address information.</span></span> <span data-ttu-id="6502b-116">Zero será retornado como o endereço de qualquer campo em branco.</span><span class="sxs-lookup"><span data-stu-id="6502b-116">Zero will be returned as the address for any blank fields.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6502b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6502b-117">Return value</span></span>

<span data-ttu-id="6502b-118">Retorna o número de campos não vazios.</span><span class="sxs-lookup"><span data-stu-id="6502b-118">Returns the number of nonblank fields.</span></span>

## <a name="requirements"></a><span data-ttu-id="6502b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6502b-119">Requirements</span></span>



| <span data-ttu-id="6502b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6502b-120">Requirement</span></span> | <span data-ttu-id="6502b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6502b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6502b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6502b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6502b-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6502b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6502b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6502b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6502b-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6502b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6502b-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6502b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6502b-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6502b-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





