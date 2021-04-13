---
title: Mensagem de EM_GETIMECOMPMODE (RichEdit. h)
description: Recupera o modo do IME (editor de método de entrada) atual para um controle de edição rico.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- Controles de EM_GETIMECOMPMODE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455545"
---
# <a name="em_getimecompmode-message"></a><span data-ttu-id="a45cb-104">\_Mensagem em GETIMECOMPMODE</span><span class="sxs-lookup"><span data-stu-id="a45cb-104">EM\_GETIMECOMPMODE message</span></span>

<span data-ttu-id="a45cb-105">Recupera o modo do IME (editor de método de entrada) atual para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="a45cb-105">Retrieves the current Input Method Editor (IME) mode for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a45cb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a45cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a45cb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a45cb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a45cb-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a45cb-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a45cb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a45cb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a45cb-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a45cb-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a45cb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a45cb-111">Return value</span></span>

<span data-ttu-id="a45cb-112">O valor de retorno é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a45cb-112">The return value is one of the following values.</span></span>



| <span data-ttu-id="a45cb-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a45cb-113">Return code</span></span>                                                                                     | <span data-ttu-id="a45cb-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a45cb-114">Description</span></span>                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="a45cb-115"><dt>**ICM não \_ aberto**</dt></span><span class="sxs-lookup"><span data-stu-id="a45cb-115"><dt>**ICM\_NOTOPEN**</dt></span></span> </dl>     | <span data-ttu-id="a45cb-116">O IME não está aberto.</span><span class="sxs-lookup"><span data-stu-id="a45cb-116">IME is not open.</span></span><br/>  |
| <dl> <span data-ttu-id="a45cb-117"><dt>**LEVEL3 de ICM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a45cb-117"><dt>**ICM\_LEVEL3**</dt></span></span> </dl>      | <span data-ttu-id="a45cb-118">Modo embutido verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="a45cb-118">True inline mode.</span></span><br/> |
| <dl> <span data-ttu-id="a45cb-119"><dt>**LEVEL2 de ICM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a45cb-119"><dt>**ICM\_LEVEL2**</dt></span></span> </dl>      | <span data-ttu-id="a45cb-120">Nível 2.</span><span class="sxs-lookup"><span data-stu-id="a45cb-120">Level 2.</span></span><br/>          |
| <dl> <span data-ttu-id="a45cb-121"><dt>**ICM \_ LEVEL2 \_ 5**</dt></span><span class="sxs-lookup"><span data-stu-id="a45cb-121"><dt>**ICM\_LEVEL2\_5**</dt></span></span> </dl>   | <span data-ttu-id="a45cb-122">Nível 2,5</span><span class="sxs-lookup"><span data-stu-id="a45cb-122">Level 2.5</span></span><br/>         |
| <dl> <span data-ttu-id="a45cb-123"><dt>**ICM \_ LEVEL2 \_ sui**</dt></span><span class="sxs-lookup"><span data-stu-id="a45cb-123"><dt>**ICM\_LEVEL2\_SUI**</dt></span></span> </dl> | <span data-ttu-id="a45cb-124">Interface do usuário especial.</span><span class="sxs-lookup"><span data-stu-id="a45cb-124">Special UI.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="a45cb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a45cb-125">Requirements</span></span>



| <span data-ttu-id="a45cb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a45cb-126">Requirement</span></span> | <span data-ttu-id="a45cb-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a45cb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a45cb-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a45cb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a45cb-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a45cb-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a45cb-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a45cb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a45cb-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a45cb-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a45cb-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a45cb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a45cb-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a45cb-133"><dt>Richedit.h</dt></span></span> </dl> |



 

 





