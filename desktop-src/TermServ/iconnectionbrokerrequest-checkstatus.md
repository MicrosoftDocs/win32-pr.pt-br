---
title: Método IConnectionBrokerRequest CheckStatus (Cbclient. h)
description: Chamado para determinar o status de uma solicitação assíncrona.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CheckStatus
- Método CheckStatus Serviços de Área de Trabalho Remota, interface IConnectionBrokerRequest
- Serviços de Área de Trabalho Remota de interface IConnectionBrokerRequest, método CheckStatus
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369876"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a><span data-ttu-id="67c28-106">Método IConnectionBrokerRequest:: CheckStatus</span><span class="sxs-lookup"><span data-stu-id="67c28-106">IConnectionBrokerRequest::CheckStatus method</span></span>

<span data-ttu-id="67c28-107">Chamado para determinar o status de uma solicitação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="67c28-107">Called to determine the status of an asynchronous request.</span></span>

## <a name="syntax"></a><span data-ttu-id="67c28-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67c28-108">Syntax</span></span>


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a><span data-ttu-id="67c28-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67c28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67c28-110">*pReqStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="67c28-110">*pReqStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67c28-111">O endereço de uma variável que recebe um valor da enumeração [**de \_ \_ status da solicitação CB**](cb-request-status.md) que indica o status da solicitação.</span><span class="sxs-lookup"><span data-stu-id="67c28-111">The address of a variable that receives a value of the [**CB\_REQUEST\_STATUS**](cb-request-status.md) enumeration that indicates the status of the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67c28-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67c28-112">Return value</span></span>

<span data-ttu-id="67c28-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="67c28-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67c28-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67c28-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="67c28-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67c28-115">Requirements</span></span>



| <span data-ttu-id="67c28-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="67c28-116">Requirement</span></span> | <span data-ttu-id="67c28-117">Valor</span><span class="sxs-lookup"><span data-stu-id="67c28-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67c28-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67c28-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67c28-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="67c28-119">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="67c28-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67c28-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67c28-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="67c28-121">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="67c28-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67c28-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="67c28-123"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="67c28-123"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="67c28-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67c28-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="67c28-125"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67c28-125"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="67c28-126">DLL</span><span class="sxs-lookup"><span data-stu-id="67c28-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67c28-127"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67c28-127"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c28-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="67c28-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c28-129">**IConnectionBrokerRequest**</span><span class="sxs-lookup"><span data-stu-id="67c28-129">**IConnectionBrokerRequest**</span></span>](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





