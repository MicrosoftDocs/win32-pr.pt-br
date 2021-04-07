---
title: Mensagem de EM_SETOLECALLBACK (RichEdit. h)
description: Fornece um controle de edição rico de um objeto IRichEditOleCallback que o controle usa para obter informações e recursos relacionados ao OLE do cliente.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- Controles de EM_SETOLECALLBACK de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918618"
---
# <a name="em_setolecallback-message"></a><span data-ttu-id="c2c58-104">\_Mensagem em SETOLECALLBACK</span><span class="sxs-lookup"><span data-stu-id="c2c58-104">EM\_SETOLECALLBACK message</span></span>

<span data-ttu-id="c2c58-105">Fornece um controle de edição rico de um objeto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) que o controle usa para obter informações e recursos relacionados ao OLE do cliente.</span><span class="sxs-lookup"><span data-stu-id="c2c58-105">Gives a rich edit control an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object that the control uses to get OLE-related resources and information from the client.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2c58-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2c58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2c58-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2c58-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2c58-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c2c58-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c2c58-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2c58-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2c58-110">Ponteiro para um objeto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) .</span><span class="sxs-lookup"><span data-stu-id="c2c58-110">Pointer to an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object.</span></span> <span data-ttu-id="c2c58-111">O controle chama o método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para o objeto antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="c2c58-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2c58-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2c58-112">Return value</span></span>

<span data-ttu-id="c2c58-113">Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c2c58-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c2c58-114">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="c2c58-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2c58-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2c58-115">Requirements</span></span>



| <span data-ttu-id="c2c58-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2c58-116">Requirement</span></span> | <span data-ttu-id="c2c58-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c2c58-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c58-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2c58-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c2c58-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2c58-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2c58-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2c58-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c2c58-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2c58-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2c58-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2c58-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2c58-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2c58-123"><dt>Richedit.h</dt></span></span> </dl> |



 

