---
title: Códigos de erro do WER (Werapi. h)
description: A tabela a seguir fornece uma lista de códigos de erro personalizados usados pelo Relatório de Erros do Windows.
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781309"
---
# <a name="wer-error-codes"></a><span data-ttu-id="8ecdf-103">Códigos de erro do WER</span><span class="sxs-lookup"><span data-stu-id="8ecdf-103">WER Error Codes</span></span>

<span data-ttu-id="8ecdf-104">A tabela a seguir fornece uma lista de códigos de erro personalizados usados pelo Relatório de Erros do Windows.</span><span class="sxs-lookup"><span data-stu-id="8ecdf-104">The following table provides a list of custom error codes used by Windows Error Reporting.</span></span>



| <span data-ttu-id="8ecdf-105">Constante</span><span class="sxs-lookup"><span data-stu-id="8ecdf-105">Constant</span></span>                                                                                                                                                                                            | <span data-ttu-id="8ecdf-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ecdf-106">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <span data-ttu-id="8ecdf-107"><dt>**WER \_ E \_ buffer insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8ecdf-107"><dt>**WER\_E\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="8ecdf-108">Um buffer é muito pequeno para conter os dados.</span><span class="sxs-lookup"><span data-stu-id="8ecdf-108">A buffer is too small to contain the data.</span></span><br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <span data-ttu-id="8ecdf-109"><dt>**WER \_ E \_ \_ estado inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="8ecdf-109"><dt>**WER\_E\_INVALID\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="8ecdf-110">Uma função foi chamada de uma maneira sem suporte.</span><span class="sxs-lookup"><span data-stu-id="8ecdf-110">A function was called in an unsupported manner.</span></span><br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <span data-ttu-id="8ecdf-111"><dt>**WER \_ E \_ comprimento \_ excedidos**</dt></span><span class="sxs-lookup"><span data-stu-id="8ecdf-111"><dt>**WER\_E\_LENGTH\_EXCEEDED**</dt></span></span> </dl>             | <span data-ttu-id="8ecdf-112">Um dos limites de comprimento foi excedido.</span><span class="sxs-lookup"><span data-stu-id="8ecdf-112">One of the length limits has been exceeded.</span></span><br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <span data-ttu-id="8ecdf-113"><dt>**parâmetro do WER \_ E \_ ausente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8ecdf-113"><dt>**WER\_E\_MISSING\_PARAM**</dt></span></span> </dl>                   | <span data-ttu-id="8ecdf-114">Um ou mais parâmetros estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="8ecdf-114">One or more parameters are missing.</span></span><br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <span data-ttu-id="8ecdf-115"><dt>**WER \_ E \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="8ecdf-115"><dt>**WER\_E\_NOT\_FOUND**</dt></span></span> </dl>                               | <span data-ttu-id="8ecdf-116">Elemento não encontrado.</span><span class="sxs-lookup"><span data-stu-id="8ecdf-116">Element not found.</span></span><br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <span data-ttu-id="8ecdf-117"><dt>**repositório do WER \_ E \_ \_ desabilitado**</dt></span><span class="sxs-lookup"><span data-stu-id="8ecdf-117"><dt>**WER\_E\_STORE\_DISABLED**</dt></span></span> </dl>                | <span data-ttu-id="8ecdf-118">O repositório foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8ecdf-118">The store has been disabled.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="8ecdf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ecdf-119">Requirements</span></span>



| <span data-ttu-id="8ecdf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ecdf-120">Requirement</span></span> | <span data-ttu-id="8ecdf-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8ecdf-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8ecdf-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ecdf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8ecdf-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ecdf-123">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8ecdf-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ecdf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8ecdf-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ecdf-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8ecdf-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ecdf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ecdf-127"><dt>Werapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ecdf-127"><dt>Werapi.h</dt></span></span> </dl> |



 

 





