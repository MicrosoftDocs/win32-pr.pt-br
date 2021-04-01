---
title: Mensagem de RB_GETBANDMARGINS (commctrl. h)
description: Recupera as margens de uma banda.
ms.assetid: 262f4180-53f9-428f-9360-75b762470270
keywords:
- Controles de RB_GETBANDMARGINS de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETBANDMARGINS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ab77c057073d9816d1310b1e8cb39fd374956b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918780"
---
# <a name="rb_getbandmargins-message"></a><span data-ttu-id="e4b81-104">\_Mensagem GETBANDMARGINS RB</span><span class="sxs-lookup"><span data-stu-id="e4b81-104">RB\_GETBANDMARGINS message</span></span>

<span data-ttu-id="e4b81-105">Recupera as margens de uma banda.</span><span class="sxs-lookup"><span data-stu-id="e4b81-105">Retrieves the margins of a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4b81-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4b81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b81-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4b81-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e4b81-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e4b81-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e4b81-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4b81-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b81-110">Ponteiro para uma estrutura de [**margens**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) que recebe as margens recuperadas.</span><span class="sxs-lookup"><span data-stu-id="e4b81-110">Pointer to a [**MARGINS**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) structure that receives the retrieved margins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b81-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4b81-111">Return value</span></span>

<span data-ttu-id="e4b81-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="e4b81-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b81-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4b81-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e4b81-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="e4b81-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e4b81-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e4b81-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e4b81-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4b81-116">Requirements</span></span>



| <span data-ttu-id="e4b81-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4b81-117">Requirement</span></span> | <span data-ttu-id="e4b81-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e4b81-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b81-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4b81-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b81-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4b81-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4b81-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4b81-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b81-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4b81-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4b81-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4b81-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b81-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b81-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





