---
title: Mensagem de EM_INSERTIMAGE (RichEdit. h)
description: Substitui a seleção por um blob que exibe uma imagem.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- Controles de EM_INSERTIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454760"
---
# <a name="em_insertimage-message"></a><span data-ttu-id="5b316-104">\_Mensagem em INSERTIMAGE</span><span class="sxs-lookup"><span data-stu-id="5b316-104">EM\_INSERTIMAGE message</span></span>

<span data-ttu-id="5b316-105">Substitui a seleção por um blob que exibe uma imagem.</span><span class="sxs-lookup"><span data-stu-id="5b316-105">Replaces the selection with a blob that displays an image.</span></span>


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a><span data-ttu-id="5b316-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b316-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b316-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b316-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b316-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5b316-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5b316-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b316-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b316-110">Um ponteiro para uma estrutura de [**\_ \_ parâmetros de imagem RichEdit**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) que contém o blob de imagem.</span><span class="sxs-lookup"><span data-stu-id="5b316-110">A pointer to a [**RICHEDIT\_IMAGE\_PARAMETERS**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) structure that contains the image blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b316-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b316-111">Return value</span></span>

<span data-ttu-id="5b316-112">Retorna S \_ OK se for bem-sucedido ou um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="5b316-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="5b316-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5b316-113">Return code</span></span>                                                                                    | <span data-ttu-id="5b316-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b316-114">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="5b316-115"><dt>**E \_ FALHA**</dt></span><span class="sxs-lookup"><span data-stu-id="5b316-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="5b316-116">Não é possível inserir a imagem.</span><span class="sxs-lookup"><span data-stu-id="5b316-116">Cannot insert the image.</span></span> <br/>                          |
| <dl> <span data-ttu-id="5b316-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5b316-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="5b316-118">O parâmetro *lParam* é nulo ou aponta para uma imagem inválida.</span><span class="sxs-lookup"><span data-stu-id="5b316-118">The *lParam* parameter is NULL or points to an invalid image.</span></span> |
| <dl> <span data-ttu-id="5b316-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5b316-119"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="5b316-120">Memória insuficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="5b316-120">Insufficient memory is available.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="5b316-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b316-121">Remarks</span></span>

<span data-ttu-id="5b316-122">Se a seleção for um ponto de inserção, o blob de imagem será inserido no ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="5b316-122">If the selection is an insertion point, the image blob is inserted at the insertion point.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b316-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b316-123">Requirements</span></span>



| <span data-ttu-id="5b316-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b316-124">Requirement</span></span> | <span data-ttu-id="5b316-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5b316-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b316-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b316-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5b316-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5b316-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5b316-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b316-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5b316-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5b316-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b316-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b316-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b316-131"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b316-131"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b316-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b316-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b316-133">**\_inserir em**</span><span class="sxs-lookup"><span data-stu-id="5b316-133">**EM\_INSERTTABLE**</span></span>](em-inserttable.md)
</dt> </dl>

 

 





