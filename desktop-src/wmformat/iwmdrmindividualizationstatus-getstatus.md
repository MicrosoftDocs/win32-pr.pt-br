---
title: Método GetStatus IWMDRMIndividualizationStatus (wmdrmsdk. h)
description: O método GetStatus recupera informações detalhadas sobre o progresso de individualização.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- Método GetStatus Windows Media Format
- Método GetStatus Windows Media Format, interface IWMDRMIndividualizationStatus
- Formato de mídia do Windows da interface IWMDRMIndividualizationStatus, método GetStatus
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765198"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a><span data-ttu-id="d4aa5-106">Método IWMDRMIndividualizationStatus:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="d4aa5-106">IWMDRMIndividualizationStatus::GetStatus method</span></span>

<span data-ttu-id="d4aa5-107">O método **GetStatus** recupera informações detalhadas sobre o progresso de individualização.</span><span class="sxs-lookup"><span data-stu-id="d4aa5-107">The **GetStatus** method retrieves detailed information about individualization progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4aa5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4aa5-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="d4aa5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4aa5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4aa5-110">*pStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d4aa5-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4aa5-111">Recebe uma estrutura de [**\_ \_ status de individualização do WM**](drmwm-individualize-status.md) que contém informações detalhadas sobre o status da tentativa de individualização.</span><span class="sxs-lookup"><span data-stu-id="d4aa5-111">Receives a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure containing detailed information about the status of the individualization attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4aa5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4aa5-112">Return value</span></span>

<span data-ttu-id="d4aa5-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d4aa5-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d4aa5-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d4aa5-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d4aa5-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d4aa5-115">Return code</span></span>                                                                          | <span data-ttu-id="d4aa5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4aa5-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d4aa5-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4aa5-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d4aa5-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d4aa5-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4aa5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4aa5-119">Remarks</span></span>

<span data-ttu-id="d4aa5-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d4aa5-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4aa5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4aa5-121">Requirements</span></span>



| <span data-ttu-id="d4aa5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4aa5-122">Requirement</span></span> | <span data-ttu-id="d4aa5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d4aa5-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aa5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4aa5-124">Header</span></span><br/> | <dl> <span data-ttu-id="d4aa5-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4aa5-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4aa5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4aa5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4aa5-127">**Interface IWMDRMIndividualizationStatus**</span><span class="sxs-lookup"><span data-stu-id="d4aa5-127">**IWMDRMIndividualizationStatus Interface**</span></span>](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





