---
title: Mensagem de STM_SETICON (WinUser. h)
description: Um aplicativo envia a \_ mensagem de AUTOÍCONE STM para associar um ícone a um controle de ícone.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- Controles de STM_SETICON de mensagens do Windows
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008920"
---
# <a name="stm_seticon-message"></a><span data-ttu-id="78047-104">\_Mensagem de SETICON STM</span><span class="sxs-lookup"><span data-stu-id="78047-104">STM\_SETICON message</span></span>

<span data-ttu-id="78047-105">Um aplicativo envia a mensagem de **\_ autoícone STM** para associar um ícone a um controle de ícone.</span><span class="sxs-lookup"><span data-stu-id="78047-105">An application sends the **STM\_SETICON** message to associate an icon with an icon control.</span></span>

## <a name="parameters"></a><span data-ttu-id="78047-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78047-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78047-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78047-108">Identificador para o ícone a ser associado ao controle de ícone.</span><span class="sxs-lookup"><span data-stu-id="78047-108">Handle to the icon to associate with the icon control.</span></span>

</dd> <dt>

<span data-ttu-id="78047-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78047-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78047-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="78047-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78047-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78047-111">Return value</span></span>

<span data-ttu-id="78047-112">O valor de retorno é um identificador para o ícone associado anteriormente ao controle de ícone ou zero se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="78047-112">The return value is a handle to the icon previously associated with the icon control, or zero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="78047-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78047-113">Requirements</span></span>



| <span data-ttu-id="78047-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="78047-114">Requirement</span></span> | <span data-ttu-id="78047-115">Valor</span><span class="sxs-lookup"><span data-stu-id="78047-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78047-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78047-116">Minimum supported client</span></span><br/> | <span data-ttu-id="78047-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78047-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="78047-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78047-118">Minimum supported server</span></span><br/> | <span data-ttu-id="78047-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78047-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="78047-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78047-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="78047-121"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78047-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78047-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="78047-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="78047-123">**Referência**</span><span class="sxs-lookup"><span data-stu-id="78047-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78047-124">**STM \_ GETicon**</span><span class="sxs-lookup"><span data-stu-id="78047-124">**STM\_GETICON**</span></span>](stm-geticon.md)
</dt> <dt>

<span data-ttu-id="78047-125">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="78047-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="78047-126">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="78047-126">**LoadIcon**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

