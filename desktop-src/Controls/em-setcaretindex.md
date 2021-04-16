---
title: Mensagem de EM_SETCARETINDEX (CommCtrl. h)
description: Define o valor de índice baseado em zero da posição do cursor em um controle de edição.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Controles de EM_SETCARETINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455767"
---
# <a name="em_setcaretindex-message"></a><span data-ttu-id="5d7d5-104">\_Mensagem em SETCARETINDEX</span><span class="sxs-lookup"><span data-stu-id="5d7d5-104">EM\_SETCARETINDEX message</span></span>

<span data-ttu-id="5d7d5-105">Define o valor de índice baseado em zero da posição do cursor em um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="5d7d5-105">Sets the zero-based index value of the position of the caret in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d7d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d7d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d7d5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d7d5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d7d5-108">O novo valor de índice baseado em zero da posição do cursor.</span><span class="sxs-lookup"><span data-stu-id="5d7d5-108">The new zero-based index value of the position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="5d7d5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d7d5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5d7d5-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5d7d5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d7d5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d7d5-111">Return value</span></span>

<span data-ttu-id="5d7d5-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5d7d5-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d7d5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d7d5-113">Remarks</span></span>

<span data-ttu-id="5d7d5-114">Se o índice estiver fora do intervalo do texto em um controle de edição, o índice será ajustado para caber dentro do intervalo do texto.</span><span class="sxs-lookup"><span data-stu-id="5d7d5-114">If the index is out of the range of the text in an edit control, the index will be adjusted to fit inside the range of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d7d5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d7d5-115">Requirements</span></span>



| <span data-ttu-id="5d7d5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d7d5-116">Requirement</span></span> | <span data-ttu-id="5d7d5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5d7d5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7d5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d7d5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7d5-119">\[Somente aplicativos de área de trabalho do Windows 10, 1809\]</span><span class="sxs-lookup"><span data-stu-id="5d7d5-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5d7d5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d7d5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7d5-121">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="5d7d5-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5d7d5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d7d5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d7d5-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d7d5-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d7d5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d7d5-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d7d5-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5d7d5-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5d7d5-126">**em \_ GETCARETINDEX**</span><span class="sxs-lookup"><span data-stu-id="5d7d5-126">**EM\_GETCARETINDEX**</span></span>](em-getcaretindex.md)
</dt> </dl>

 

 





