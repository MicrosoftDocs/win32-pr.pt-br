---
title: Mensagem de CQPM_PERSIST (Cmnquery. h)
description: Enviado para a função de retorno de chamada CQPageProc de uma página de extensão de formulário de consulta para permitir que a página leia ou grave dados de consulta de memória persistente.
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_PERSIST Active Directory
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70aaaae3b4fcc6788a16d59477d5f8158b43b892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009311"
---
# <a name="cqpm_persist-message"></a><span data-ttu-id="67cef-104">CQPM \_ manter mensagem</span><span class="sxs-lookup"><span data-stu-id="67cef-104">CQPM\_PERSIST message</span></span>

<span data-ttu-id="67cef-105">A mensagem de **\_ persistência CQPM** é enviada para a função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de uma página de extensão de formulário de consulta para permitir que a página leia ou grave dados de consulta de memória persistente.</span><span class="sxs-lookup"><span data-stu-id="67cef-105">The **CQPM\_PERSIST** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page to read or write query data from persistent memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="67cef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67cef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67cef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67cef-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67cef-108">Contém um valor diferente de zero para ler os dados da consulta ou zero para gravar os dados da consulta.</span><span class="sxs-lookup"><span data-stu-id="67cef-108">Contains nonzero to read the query data or zero to write the query data.</span></span>

</dd> <dt>

<span data-ttu-id="67cef-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67cef-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67cef-110">Ponteiro para uma interface [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) na qual os dados da consulta devem ser lidos ou gravados.</span><span class="sxs-lookup"><span data-stu-id="67cef-110">Pointer to an [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) interface that the query data should be read from or written to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67cef-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67cef-111">Return value</span></span>

<span data-ttu-id="67cef-112">Retorna **S \_ OK** se for bem-sucedido ou um código de erro **HRESULT** padrão do contrário.</span><span class="sxs-lookup"><span data-stu-id="67cef-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="67cef-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67cef-113">Requirements</span></span>



| <span data-ttu-id="67cef-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="67cef-114">Requirement</span></span> | <span data-ttu-id="67cef-115">Valor</span><span class="sxs-lookup"><span data-stu-id="67cef-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67cef-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67cef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67cef-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67cef-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="67cef-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67cef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67cef-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67cef-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="67cef-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67cef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="67cef-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="67cef-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67cef-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="67cef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67cef-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="67cef-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="67cef-124">**IPersistQuery**</span><span class="sxs-lookup"><span data-stu-id="67cef-124">**IPersistQuery**</span></span>](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

