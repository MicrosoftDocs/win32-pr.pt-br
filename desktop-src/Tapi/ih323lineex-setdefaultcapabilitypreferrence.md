---
description: Configura a preferência dos recursos padrão.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'Método IH323LineEx:: SetDefaultCapabilityPreferrence (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756997"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a><span data-ttu-id="11214-103">Método IH323LineEx:: SetDefaultCapabilityPreferrence</span><span class="sxs-lookup"><span data-stu-id="11214-103">IH323LineEx::SetDefaultCapabilityPreferrence method</span></span>

<span data-ttu-id="11214-104">\[O **SetDefaultCapabilityPreferrence** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="11214-104">\[**SetDefaultCapabilityPreferrence** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="11214-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="11214-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="11214-106">O método **SetDefaultCapabilityPreferrence** configura a preferência dos recursos padrão.</span><span class="sxs-lookup"><span data-stu-id="11214-106">The **SetDefaultCapabilityPreferrence** method configures the preference of the default capabilities.</span></span> <span data-ttu-id="11214-107">Os recursos têm um peso padrão de 100.</span><span class="sxs-lookup"><span data-stu-id="11214-107">Capabilities have a default weight of 100.</span></span> <span data-ttu-id="11214-108">Se o aplicativo especificar um peso mais alto para um recurso, ele terá uma prioridade mais alta durante a negociação H. 245.</span><span class="sxs-lookup"><span data-stu-id="11214-108">If the application specifies a higher weight for a capability, it will have a higher priority during the H.245 negotiation.</span></span> <span data-ttu-id="11214-109">Se o aplicativo definir o peso de um recurso como 0, ele não será usado na negociação H. 245.</span><span class="sxs-lookup"><span data-stu-id="11214-109">If the application sets the weight of a capability to 0, it will not be used in the H.245 negotiation.</span></span>

<span data-ttu-id="11214-110">Esse método é cumulativo.</span><span class="sxs-lookup"><span data-stu-id="11214-110">This method is cumulative.</span></span> <span data-ttu-id="11214-111">Por exemplo, se esse método for chamado primeiro para desabilitar um recurso e for chamado novamente para desabilitar outro, ambos os recursos serão desabilitados como resultado dessas duas chamadas.</span><span class="sxs-lookup"><span data-stu-id="11214-111">For example, if this method is called first to disable a capability and is called again to disable another, both capabilities will be disabled as the result of these two calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="11214-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11214-112">Syntax</span></span>


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="11214-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11214-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11214-114">*dwNumCaps* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11214-114">*dwNumCaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11214-115">Um valor **DWORD** que contém o número de recursos definidos com este método.</span><span class="sxs-lookup"><span data-stu-id="11214-115">A **DWORD** value that contains the number of capabilities set with this method.</span></span>

</dd> <dt>

<span data-ttu-id="11214-116">*pCapabilities* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11214-116">*pCapabilities* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11214-117">Uma matriz de recursos.</span><span class="sxs-lookup"><span data-stu-id="11214-117">An array of capabilities.</span></span> <span data-ttu-id="11214-118">Cada elemento da matriz é um valor [**de \_ recurso H245**](h245-capability.md) .</span><span class="sxs-lookup"><span data-stu-id="11214-118">Each element of the array is an [**H245\_CAPABILITY**](h245-capability.md) value.</span></span>

</dd> <dt>

<span data-ttu-id="11214-119">*pWeights* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11214-119">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11214-120">Uma matriz de pesos associada aos recursos.</span><span class="sxs-lookup"><span data-stu-id="11214-120">An array of weights associated with the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11214-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11214-121">Return value</span></span>

<span data-ttu-id="11214-122">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="11214-122">This method can return one of these values.</span></span>



| <span data-ttu-id="11214-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="11214-123">Return code</span></span>                                                                                   | <span data-ttu-id="11214-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="11214-124">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11214-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11214-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="11214-126">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="11214-126">Method succeeded.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="11214-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="11214-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="11214-128">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="11214-128">Insufficient memory exists to perform the operation.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="11214-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="11214-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="11214-130">O parâmetro *pCapabilities* é **nulo** ou o parâmetro *pWeights* é **nulo** ou *pCapabilities* e *pWeights* são **nulos** ou a matriz pCapabilities contém um objeto de recurso H. 245 inválido.</span><span class="sxs-lookup"><span data-stu-id="11214-130">The *pCapabilities* parameter is **NULL**, or the *pWeights* parameter is **NULL**, or both *pCapabilities* and *pWeights* are **NULL**, or the pCapabilities array contains an invalid H.245 capability object.</span></span><br/> |
| <dl> <span data-ttu-id="11214-131"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="11214-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="11214-132">Não é possível ler um elemento da matriz *pWeights* ou de um elemento da matriz *pCapabilities* .</span><span class="sxs-lookup"><span data-stu-id="11214-132">Unable to read an element of the *pWeights* array or an element of the *pCapabilities* array.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="11214-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11214-133">Requirements</span></span>



| <span data-ttu-id="11214-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="11214-134">Requirement</span></span> | <span data-ttu-id="11214-135">Valor</span><span class="sxs-lookup"><span data-stu-id="11214-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11214-136">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="11214-136">TAPI version</span></span><br/> | <span data-ttu-id="11214-137">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="11214-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="11214-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11214-138">Header</span></span><br/>       | <dl> <span data-ttu-id="11214-139"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="11214-139"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="11214-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11214-140">Library</span></span><br/>      | <dl> <span data-ttu-id="11214-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11214-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="11214-142">DLL</span><span class="sxs-lookup"><span data-stu-id="11214-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="11214-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11214-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




