---
title: Método IWMDRMNetTransmitter GetLeafLicenseResponse (wmdrmsdk. h)
description: O método GetLeafLicenseResponse gera uma mensagem de resposta de licença de folha.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Formato de mídia do Windows do método GetLeafLicenseResponse
- Método GetLeafLicenseResponse Windows Media Format, interface IWMDRMNetTransmitter
- Formato de mídia do Windows de interface IWMDRMNetTransmitter, método GetLeafLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785316"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a><span data-ttu-id="f984f-106">Método IWMDRMNetTransmitter:: GetLeafLicenseResponse</span><span class="sxs-lookup"><span data-stu-id="f984f-106">IWMDRMNetTransmitter::GetLeafLicenseResponse method</span></span>

<span data-ttu-id="f984f-107">O método **GetLeafLicenseResponse** gera uma mensagem de resposta de licença de folha.</span><span class="sxs-lookup"><span data-stu-id="f984f-107">The **GetLeafLicenseResponse** method generates a leaf license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="f984f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f984f-108">Syntax</span></span>


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="f984f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f984f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f984f-110">*bstrKID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f984f-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f984f-111">Identificador de chave codificado em base64 a ser usado para a nova licença de folha.</span><span class="sxs-lookup"><span data-stu-id="f984f-111">Base64-encoded key identifier to be used for the new leaf license.</span></span> <span data-ttu-id="f984f-112">O identificador de chave deve ser um valor GUID gerado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="f984f-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="f984f-113">*pPolicy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f984f-113">*pPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f984f-114">Ponteiro para a estrutura de [**\_ política WMDRMNET**](wmdrmnet-policy.md) que define a política a ser usada para a licença de folha.</span><span class="sxs-lookup"><span data-stu-id="f984f-114">Pointer to the [**WMDRMNET\_POLICY**](wmdrmnet-policy.md) structure that defines the policy to use for the leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="f984f-115">*ppIWMDRMEncrypt* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f984f-115">*ppIWMDRMEncrypt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f984f-116">Endereço de uma variável que recebe um ponteiro para a interface [**IWMDRMEncrypt**](iwmdrmencrypt.md) que pode ser usada para criptografar dados para a nova licença de folha.</span><span class="sxs-lookup"><span data-stu-id="f984f-116">Address of a variable that receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface that can be used to encrypt data for the new leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="f984f-117">*ppbLicenseResponse* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f984f-117">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f984f-118">Endereço de uma variável que recebe o endereço da resposta de licença gerada.</span><span class="sxs-lookup"><span data-stu-id="f984f-118">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="f984f-119">Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="f984f-119">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="f984f-120">*pcbLicenseResponse* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f984f-120">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f984f-121">Endereço de uma variável que recebe o tamanho da resposta de licença, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f984f-121">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f984f-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f984f-122">Return value</span></span>

<span data-ttu-id="f984f-123">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f984f-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f984f-124">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f984f-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f984f-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f984f-125">Return code</span></span>                                                                                                | <span data-ttu-id="f984f-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="f984f-126">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="f984f-127"><dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="f984f-127"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="f984f-128">Uma lista de revogação de conteúdo atualizada é necessária.</span><span class="sxs-lookup"><span data-stu-id="f984f-128">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="f984f-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f984f-129"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="f984f-130">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f984f-130">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="f984f-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="f984f-131">Remarks</span></span>

<span data-ttu-id="f984f-132">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f984f-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f984f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f984f-133">Requirements</span></span>



| <span data-ttu-id="f984f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f984f-134">Requirement</span></span> | <span data-ttu-id="f984f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f984f-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f984f-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f984f-136">Header</span></span><br/> | <dl> <span data-ttu-id="f984f-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f984f-137"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f984f-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f984f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f984f-139">**Interface IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="f984f-139">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





