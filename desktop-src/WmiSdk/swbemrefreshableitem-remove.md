---
description: O método SWbemRefreshableItem. Remove remove o objeto SWbemRefreshableItem do objeto pai SWbemRefresher. Objeto SWbemRefreshableItem do objeto SWbemRefresher pai.
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: Método SWbemRefreshableItem. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105785023"
---
# <a name="swbemrefreshableitemremove-method"></a><span data-ttu-id="12e1e-103">Método SWbemRefreshableItem. Remove</span><span class="sxs-lookup"><span data-stu-id="12e1e-103">SWbemRefreshableItem.Remove method</span></span>

<span data-ttu-id="12e1e-104">O método **SWbemRefreshableItem. Remove** remove o objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) do objeto pai [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="12e1e-104">The **SWbemRefreshableItem.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object from the parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="12e1e-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="12e1e-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="12e1e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12e1e-106">Syntax</span></span>


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="12e1e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12e1e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12e1e-108">*lFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="12e1e-108">*lFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="12e1e-109">Esse parâmetro deve ser definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="12e1e-109">This parameter must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12e1e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12e1e-110">Return value</span></span>

<span data-ttu-id="12e1e-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="12e1e-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12e1e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="12e1e-112">Remarks</span></span>

<span data-ttu-id="12e1e-113">**Códigos de erro** Se o atualizador não tiver nenhum item com o índice especificado, **wbemErrNotFound** será gerado.</span><span class="sxs-lookup"><span data-stu-id="12e1e-113">**Error Codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="12e1e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12e1e-114">Requirements</span></span>



| <span data-ttu-id="12e1e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="12e1e-115">Requirement</span></span> | <span data-ttu-id="12e1e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="12e1e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12e1e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12e1e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="12e1e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12e1e-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12e1e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12e1e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="12e1e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12e1e-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12e1e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12e1e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="12e1e-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="12e1e-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="12e1e-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="12e1e-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="12e1e-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="12e1e-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="12e1e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="12e1e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12e1e-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12e1e-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="12e1e-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="12e1e-127">CLSID</span></span><br/>                    | <span data-ttu-id="12e1e-128">\_SWBEMREFRESHABLEITEM CLSID</span><span class="sxs-lookup"><span data-stu-id="12e1e-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="12e1e-129">IID</span><span class="sxs-lookup"><span data-stu-id="12e1e-129">IID</span></span><br/>                      | <span data-ttu-id="12e1e-130">ISWbemRefreshableItem de IID \_</span><span class="sxs-lookup"><span data-stu-id="12e1e-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="12e1e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="12e1e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e1e-132">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="12e1e-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="12e1e-133">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="12e1e-133">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




