---
title: Mensagem de EM_GETOLEINTERFACE (RichEdit. h)
description: Recupera um objeto IRichEditOle que um cliente pode usar para acessar uma funcionalidade COM (Component Object Model de controle de edição rica).
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- Controles de EM_GETOLEINTERFACE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085935"
---
# <a name="em_getoleinterface-message"></a><span data-ttu-id="1ec4c-104">\_Mensagem em GETOLEINTERFACE</span><span class="sxs-lookup"><span data-stu-id="1ec4c-104">EM\_GETOLEINTERFACE message</span></span>

<span data-ttu-id="1ec4c-105">Recupera um objeto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) que um cliente pode usar para acessar uma funcionalidade COM (Component Object Model de controle de edição rica).</span><span class="sxs-lookup"><span data-stu-id="1ec4c-105">Retrieves an [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object that a client can use to access a rich edit control's Component Object Model (COM) functionality.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ec4c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ec4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec4c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ec4c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec4c-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1ec4c-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1ec4c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ec4c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec4c-110">Ponteiro para um ponteiro que recebe o objeto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="1ec4c-110">Pointer to a pointer that receives the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object.</span></span> <span data-ttu-id="1ec4c-111">O controle chama o método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para o objeto antes de retornar, portanto, o aplicativo de chamada deve chamar o método [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quando ele é feito com o objeto.</span><span class="sxs-lookup"><span data-stu-id="1ec4c-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning, so the calling application must call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method when it is done with the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec4c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ec4c-112">Return value</span></span>

<span data-ttu-id="1ec4c-113">Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="1ec4c-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1ec4c-114">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="1ec4c-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec4c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ec4c-115">Requirements</span></span>



| <span data-ttu-id="1ec4c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec4c-116">Requirement</span></span> | <span data-ttu-id="1ec4c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1ec4c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec4c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ec4c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec4c-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ec4c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ec4c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ec4c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec4c-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ec4c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ec4c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ec4c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ec4c-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec4c-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec4c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ec4c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec4c-125">**IRichEditOle**</span><span class="sxs-lookup"><span data-stu-id="1ec4c-125">**IRichEditOle**</span></span>](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

