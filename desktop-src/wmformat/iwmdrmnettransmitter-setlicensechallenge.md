---
title: Método IWMDRMNetTransmitter SetLicenseChallenge (wmdrmsdk. h)
description: O método SetLicenseChallenge processa um desafio de licença enviado por um receptor do Windows Media DRM para dispositivos de rede.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Formato de mídia do Windows do método SetLicenseChallenge
- Método SetLicenseChallenge Windows Media Format, interface IWMDRMNetTransmitter
- Formato de mídia do Windows de interface IWMDRMNetTransmitter, método SetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789913"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a><span data-ttu-id="232af-106">Método IWMDRMNetTransmitter:: SetLicenseChallenge</span><span class="sxs-lookup"><span data-stu-id="232af-106">IWMDRMNetTransmitter::SetLicenseChallenge method</span></span>

<span data-ttu-id="232af-107">O método **SetLicenseChallenge** processa um desafio de licença enviado por um receptor do Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="232af-107">The **SetLicenseChallenge** method processes a license challenge sent by a Windows Media DRM for Network Devices receiver.</span></span>

## <a name="syntax"></a><span data-ttu-id="232af-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="232af-108">Syntax</span></span>


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="232af-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="232af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="232af-110">*pbLicenseChallenge* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="232af-110">*pbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="232af-111">Ponteiro para os dados de desafio de licença que foram enviados por um receptor.</span><span class="sxs-lookup"><span data-stu-id="232af-111">Pointer to the license challenge data that was sent by a receiver.</span></span>

</dd> <dt>

<span data-ttu-id="232af-112">*cbLicenseChallenge* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="232af-112">*cbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="232af-113">Tamanho do desafio de licença em bytes.</span><span class="sxs-lookup"><span data-stu-id="232af-113">Size of license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="232af-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="232af-114">Return value</span></span>

<span data-ttu-id="232af-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="232af-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="232af-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="232af-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="232af-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="232af-117">Return code</span></span>                                                                          | <span data-ttu-id="232af-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="232af-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="232af-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="232af-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="232af-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="232af-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="232af-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="232af-121">Remarks</span></span>

<span data-ttu-id="232af-122">Se esse método tiver sucesso, as chamadas subsequentes para os outros métodos de **IWMDRMNetTransmitter** usarão as informações no desafio processado.</span><span class="sxs-lookup"><span data-stu-id="232af-122">If this method succeeds, subsequent calls to the other methods of **IWMDRMNetTransmitter** will use the information in the processed challenge.</span></span>

## <a name="requirements"></a><span data-ttu-id="232af-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="232af-123">Requirements</span></span>



| <span data-ttu-id="232af-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="232af-124">Requirement</span></span> | <span data-ttu-id="232af-125">Valor</span><span class="sxs-lookup"><span data-stu-id="232af-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="232af-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="232af-126">Header</span></span><br/> | <dl> <span data-ttu-id="232af-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="232af-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="232af-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="232af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="232af-129">**Interface IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="232af-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





