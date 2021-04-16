---
title: Método IWMDRMEventGenerator CancelAsyncOperation (wmdrmsdk. h)
description: O método CancelAsyncOperation cancela uma operação assíncrona.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Formato de mídia do Windows do método CancelAsyncOperation
- Método CancelAsyncOperation Windows Media Format, interface IWMDRMEventGenerator
- Formato de mídia do Windows de interface IWMDRMEventGenerator, método CancelAsyncOperation
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750983"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a><span data-ttu-id="4f931-106">Método IWMDRMEventGenerator:: CancelAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="4f931-106">IWMDRMEventGenerator::CancelAsyncOperation method</span></span>

<span data-ttu-id="4f931-107">O método **CancelAsyncOperation** cancela uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="4f931-107">The **CancelAsyncOperation** method cancels an asynchronous operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f931-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f931-108">Syntax</span></span>


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="4f931-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f931-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f931-110">*punkCancelationCookie* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f931-110">*punkCancelationCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f931-111">Ponteiro para o cookie de cancelamento que identifica a operação assíncrona a ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="4f931-111">Pointer to the cancellation cookie that identifies the asynchronous operation to be canceled.</span></span> <span data-ttu-id="4f931-112">Esse cookie é fornecido pelo método usado para iniciar a operação.</span><span class="sxs-lookup"><span data-stu-id="4f931-112">This cookie is provided by the method used to start the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f931-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f931-113">Return value</span></span>

<span data-ttu-id="4f931-114">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4f931-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4f931-115">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4f931-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4f931-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4f931-116">Return code</span></span>                                                                          | <span data-ttu-id="4f931-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f931-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4f931-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f931-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4f931-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4f931-119">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f931-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f931-120">Remarks</span></span>

<span data-ttu-id="4f931-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4f931-121">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f931-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f931-122">Requirements</span></span>



| <span data-ttu-id="4f931-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f931-123">Requirement</span></span> | <span data-ttu-id="4f931-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4f931-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f931-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f931-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4f931-126"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f931-126"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f931-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f931-127">Library</span></span><br/> | <dl> <span data-ttu-id="4f931-128"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f931-128"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f931-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f931-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f931-130">**Interface IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="4f931-130">**IWMDRMEventGenerator Interface**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





