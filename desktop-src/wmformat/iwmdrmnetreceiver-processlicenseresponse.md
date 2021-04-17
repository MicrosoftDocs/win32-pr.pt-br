---
title: Método IWMDRMNetReceiver ProcessLicenseResponse (wmdrmsdk. h)
description: O método ProcessLicenseResponse processa a resposta de licença que é enviada pelo transmissor em resposta a um desafio de licença.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Formato de mídia do Windows do método ProcessLicenseResponse
- Método ProcessLicenseResponse Windows Media Format, interface IWMDRMNetReceiver
- Formato de mídia do Windows de interface IWMDRMNetReceiver, método ProcessLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09ebab81b71e21b9ef922423a7bbe67b20596
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770045"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a><span data-ttu-id="961c2-106">IWMDRMNetReceiver: método rocessLicenseResponse de:P</span><span class="sxs-lookup"><span data-stu-id="961c2-106">IWMDRMNetReceiver::ProcessLicenseResponse method</span></span>

<span data-ttu-id="961c2-107">O método **ProcessLicenseResponse** processa a resposta de licença que é enviada pelo transmissor em resposta a um desafio de licença.</span><span class="sxs-lookup"><span data-stu-id="961c2-107">The **ProcessLicenseResponse** method processes the license response that is sent by the transmitter in reply to a license challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="961c2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="961c2-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a><span data-ttu-id="961c2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="961c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="961c2-110">*pbLicenseResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="961c2-110">*pbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="961c2-111">Resposta de licença recebida do transmissor.</span><span class="sxs-lookup"><span data-stu-id="961c2-111">License response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="961c2-112">*cbLicenseResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="961c2-112">*cbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="961c2-113">Tamanho da resposta em bytes.</span><span class="sxs-lookup"><span data-stu-id="961c2-113">Size of the response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="961c2-114">*ppbWMDRMNetLicenseRepresentation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="961c2-114">*ppbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="961c2-115">Endereço de uma variável que recebe o endereço da representação de licença interna para a licença contida na mensagem de resposta da licença.</span><span class="sxs-lookup"><span data-stu-id="961c2-115">Address of a variable that receives the address of the internal license representation for the license contained in the license response message.</span></span> <span data-ttu-id="961c2-116">Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="961c2-116">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span> <span data-ttu-id="961c2-117">Esse parâmetro poderá ser definido como **nulo** se a representação de licença não for necessária.</span><span class="sxs-lookup"><span data-stu-id="961c2-117">This parameter may be set to **NULL** if the license representation is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="961c2-118">*pcbWMDRMNetLicenseRepresentation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="961c2-118">*pcbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="961c2-119">Endereço de uma variável que recebe o tamanho da representação de licença.</span><span class="sxs-lookup"><span data-stu-id="961c2-119">Address of a variable that receives the size of the license representation.</span></span> <span data-ttu-id="961c2-120">Deve ser definido como **NULL** se *ppbWMDRMNetLicenseRepresentation* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="961c2-120">Must be set to **NULL** if *ppbWMDRMNetLicenseRepresentation* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="961c2-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="961c2-121">Return value</span></span>

<span data-ttu-id="961c2-122">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="961c2-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="961c2-123">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="961c2-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="961c2-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="961c2-124">Return code</span></span>                                                                                                | <span data-ttu-id="961c2-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="961c2-125">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="961c2-126"><dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="961c2-126"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="961c2-127">Uma lista de revogação de conteúdo atualizada é necessária.</span><span class="sxs-lookup"><span data-stu-id="961c2-127">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="961c2-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="961c2-128"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="961c2-129">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="961c2-129">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="961c2-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="961c2-130">Remarks</span></span>

<span data-ttu-id="961c2-131">A resposta de licença processada usando esse método deve corresponder ao último desafio de licença gerado no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="961c2-131">The license response processed by using this method must correspond to the last license challenge generated on the client computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="961c2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="961c2-132">Requirements</span></span>



| <span data-ttu-id="961c2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="961c2-133">Requirement</span></span> | <span data-ttu-id="961c2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="961c2-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="961c2-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="961c2-135">Header</span></span><br/> | <dl> <span data-ttu-id="961c2-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="961c2-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="961c2-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="961c2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="961c2-138">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="961c2-138">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="961c2-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="961c2-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





