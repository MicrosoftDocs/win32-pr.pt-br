---
title: Método IWMDRMNetReceiver GetRegistrationChallenge (wmdrmsdk. h)
description: O método GetRegistrationChallenge gera uma mensagem de desafio de registro do DRM do Windows Media para dispositivos de rede.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Formato de mídia do Windows do método GetRegistrationChallenge
- Método GetRegistrationChallenge Windows Media Format, interface IWMDRMNetReceiver
- Formato de mídia do Windows de interface IWMDRMNetReceiver, método GetRegistrationChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760721"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a><span data-ttu-id="6ebda-106">Método IWMDRMNetReceiver:: GetRegistrationChallenge</span><span class="sxs-lookup"><span data-stu-id="6ebda-106">IWMDRMNetReceiver::GetRegistrationChallenge method</span></span>

<span data-ttu-id="6ebda-107">O método **GetRegistrationChallenge** gera uma mensagem de desafio de registro do DRM do Windows Media para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="6ebda-107">The **GetRegistrationChallenge** method generates a Windows Media DRM for Network Devices registration challenge message.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ebda-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ebda-108">Syntax</span></span>


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="6ebda-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ebda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ebda-110">*ppbRegistrationChallenge* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6ebda-110">*ppbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ebda-111">Endereço de um ponteiro que recebe o endereço do desafio gerado.</span><span class="sxs-lookup"><span data-stu-id="6ebda-111">Address of a pointer that receives the address of the generated challenge.</span></span> <span data-ttu-id="6ebda-112">Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="6ebda-112">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="6ebda-113">*pcbRegistrationChallenge* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6ebda-113">*pcbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ebda-114">Endereço de uma variável que recebe o tamanho do desafio de registro em bytes.</span><span class="sxs-lookup"><span data-stu-id="6ebda-114">Address of a variable that receives the size of the registration challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ebda-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ebda-115">Return value</span></span>

<span data-ttu-id="6ebda-116">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6ebda-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6ebda-117">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ebda-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6ebda-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6ebda-118">Return code</span></span>                                                                          | <span data-ttu-id="6ebda-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ebda-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6ebda-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6ebda-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6ebda-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6ebda-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6ebda-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ebda-122">Remarks</span></span>

<span data-ttu-id="6ebda-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6ebda-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ebda-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ebda-124">Requirements</span></span>



| <span data-ttu-id="6ebda-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ebda-125">Requirement</span></span> | <span data-ttu-id="6ebda-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6ebda-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebda-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ebda-127">Header</span></span><br/> | <dl> <span data-ttu-id="6ebda-128"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ebda-128"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ebda-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ebda-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ebda-130">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="6ebda-130">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="6ebda-131">**IWMDRMNetReceiver::P rocessRegistrationResponse**</span><span class="sxs-lookup"><span data-stu-id="6ebda-131">**IWMDRMNetReceiver::ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





