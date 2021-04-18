---
title: Método IWMDRMNetTransmitter GetRootLicenseResponse (wmdrmsdk. h)
description: O método GetRootLicenseResponse gera uma mensagem de resposta de licença raiz.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Formato de mídia do Windows do método GetRootLicenseResponse
- Método GetRootLicenseResponse Windows Media Format, interface IWMDRMNetTransmitter
- Formato de mídia do Windows de interface IWMDRMNetTransmitter, método GetRootLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767003"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a><span data-ttu-id="b9ae6-106">Método IWMDRMNetTransmitter:: GetRootLicenseResponse</span><span class="sxs-lookup"><span data-stu-id="b9ae6-106">IWMDRMNetTransmitter::GetRootLicenseResponse method</span></span>

<span data-ttu-id="b9ae6-107">O método **GetRootLicenseResponse** gera uma mensagem de resposta de licença raiz.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-107">The **GetRootLicenseResponse** method generates a root license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ae6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9ae6-108">Syntax</span></span>


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="b9ae6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9ae6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ae6-110">*bstrKID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9ae6-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ae6-111">Identificador de chave codificado em base64 a ser usado para a nova licença raiz.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-111">Base64-encoded key identifier to be used for the new root license.</span></span> <span data-ttu-id="b9ae6-112">O identificador de chave deve ser um valor GUID gerado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="b9ae6-113">*ppbLicenseResponse* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b9ae6-113">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ae6-114">Endereço de uma variável que recebe o endereço da resposta de licença gerada.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-114">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="b9ae6-115">Quando terminar com esses dados, você deverá liberar a memória chamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-115">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="b9ae6-116">*pcbLicenseResponse* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b9ae6-116">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ae6-117">Endereço de uma variável que recebe o tamanho da resposta de licença, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-117">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ae6-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9ae6-118">Return value</span></span>

<span data-ttu-id="b9ae6-119">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b9ae6-120">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b9ae6-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b9ae6-121">Return code</span></span>                                                                                                | <span data-ttu-id="b9ae6-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9ae6-122">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="b9ae6-123"><dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ae6-123"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="b9ae6-124">Uma lista de revogação de conteúdo atualizada é necessária.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-124">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="b9ae6-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ae6-125"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="b9ae6-126">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-126">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="b9ae6-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9ae6-127">Remarks</span></span>

<span data-ttu-id="b9ae6-128">A licença raiz gerada é criada usando as informações dos dados de desafio de licença, que são processados para a interface chamando [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).</span><span class="sxs-lookup"><span data-stu-id="b9ae6-128">The generated root license is created using the information from the license challenge data, which is processed for the interface by calling [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).</span></span>

<span data-ttu-id="b9ae6-129">A licença raiz é usada na geração de licenças de folha, que é realizada chamando o método [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="b9ae6-129">The root license is used in the generation of leaf licenses, which is accomplished by calling the [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span> <span data-ttu-id="b9ae6-130">A interface **IWMDRMNetTransmitter** mantém uma cópia da licença raiz para esse uso.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-130">The **IWMDRMNetTransmitter** interface maintains a copy of the root license for that use.</span></span>

<span data-ttu-id="b9ae6-131">A licença raiz criada chamando esse método não tem nenhuma política e está configurada para que não possa ser persistida no dispositivo receptor.</span><span class="sxs-lookup"><span data-stu-id="b9ae6-131">The root license created by calling this method does not have any policies and is configured so that it cannot be persisted on the receiving device.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ae6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9ae6-132">Requirements</span></span>



| <span data-ttu-id="b9ae6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9ae6-133">Requirement</span></span> | <span data-ttu-id="b9ae6-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b9ae6-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ae6-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9ae6-135">Header</span></span><br/> | <dl> <span data-ttu-id="b9ae6-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ae6-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9ae6-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9ae6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ae6-138">**Interface IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="b9ae6-138">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





