---
title: Mensagem de EM_EXSETSEL (RichEdit. h)
description: Seleciona um intervalo de caracteres ou objetos de Component Object Model (COM) em um controle de edição rico da Microsoft.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- Controles de EM_EXSETSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824532"
---
# <a name="em_exsetsel-message"></a><span data-ttu-id="4ff22-104">\_Mensagem em EXSETSEL</span><span class="sxs-lookup"><span data-stu-id="4ff22-104">EM\_EXSETSEL message</span></span>

<span data-ttu-id="4ff22-105">Seleciona um intervalo de caracteres ou objetos de Component Object Model (COM) em um controle de edição rico da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4ff22-105">Selects a range of characters or Component Object Model (COM) objects in a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ff22-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ff22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ff22-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ff22-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ff22-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4ff22-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4ff22-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ff22-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ff22-110">Uma estrutura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que especifica o intervalo de seleção.</span><span class="sxs-lookup"><span data-stu-id="4ff22-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that specifies the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ff22-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ff22-111">Return value</span></span>

<span data-ttu-id="4ff22-112">O valor de retorno é a seleção que realmente está definida.</span><span class="sxs-lookup"><span data-stu-id="4ff22-112">The return value is the selection that is actually set.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ff22-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ff22-113">Requirements</span></span>



| <span data-ttu-id="4ff22-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ff22-114">Requirement</span></span> | <span data-ttu-id="4ff22-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4ff22-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ff22-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ff22-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4ff22-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ff22-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4ff22-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ff22-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4ff22-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4ff22-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ff22-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ff22-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ff22-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ff22-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





