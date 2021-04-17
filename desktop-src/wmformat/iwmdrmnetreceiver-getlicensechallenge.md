---
title: Método IWMDRMNetReceiver GetLicenseChallenge (wmdrmsdk. h)
description: O método GetLicenseChallenge gera um desafio de licença do Windows Media DRM para dispositivos de rede que pode ser enviado para um transmissor ao solicitar conteúdo protegido.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Formato de mídia do Windows do método GetLicenseChallenge
- Método GetLicenseChallenge Windows Media Format, interface IWMDRMNetReceiver
- Formato de mídia do Windows de interface IWMDRMNetReceiver, método GetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766284"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a><span data-ttu-id="04106-106">Método IWMDRMNetReceiver:: GetLicenseChallenge</span><span class="sxs-lookup"><span data-stu-id="04106-106">IWMDRMNetReceiver::GetLicenseChallenge method</span></span>

<span data-ttu-id="04106-107">O método **GetLicenseChallenge** gera um desafio de licença do Windows Media DRM para dispositivos de rede que pode ser enviado para um transmissor ao solicitar conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="04106-107">The **GetLicenseChallenge** method generates a Windows Media DRM for Network Devices license challenge that can be sent to a transmitter when requesting protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="04106-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04106-108">Syntax</span></span>


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="04106-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04106-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04106-110">*bstrAction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04106-110">*bstrAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04106-111">Ação para a qual gerar o desafio.</span><span class="sxs-lookup"><span data-stu-id="04106-111">Action for which to generate the challenge.</span></span>

</dd> <dt>

<span data-ttu-id="04106-112">*ppbLicenseChallenge* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04106-112">*ppbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04106-113">Endereço de um ponteiro que é definido como o endereço do desafio gerado.</span><span class="sxs-lookup"><span data-stu-id="04106-113">Address of a pointer that is set to the address of the generated challenge.</span></span> <span data-ttu-id="04106-114">Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="04106-114">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="04106-115">*pcbLicenseChallenge* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04106-115">*pcbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04106-116">Endereço de uma variável que recebe o tamanho do desafio de licença em bytes.</span><span class="sxs-lookup"><span data-stu-id="04106-116">Address of a variable that receives the size of the license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04106-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04106-117">Return value</span></span>

<span data-ttu-id="04106-118">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="04106-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="04106-119">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="04106-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="04106-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="04106-120">Return code</span></span>                                                                          | <span data-ttu-id="04106-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="04106-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="04106-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04106-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="04106-123">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="04106-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="04106-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="04106-124">Remarks</span></span>

<span data-ttu-id="04106-125">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="04106-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="04106-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04106-126">Requirements</span></span>



| <span data-ttu-id="04106-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="04106-127">Requirement</span></span> | <span data-ttu-id="04106-128">Valor</span><span class="sxs-lookup"><span data-stu-id="04106-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04106-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04106-129">Header</span></span><br/> | <dl> <span data-ttu-id="04106-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="04106-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04106-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="04106-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04106-132">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="04106-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="04106-133">**IWMDRMNetReceiver::P rocessLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="04106-133">**IWMDRMNetReceiver::ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





