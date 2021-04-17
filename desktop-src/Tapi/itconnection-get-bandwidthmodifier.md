---
description: O \_ método Get BandwidthModifier Obtém o modificador de largura de banda, que é uma única palavra alfanumérica fornecendo o significado da figura de largura de banda. Os dois modificadores definidos são CT (total da conferência) e AS (máximo específico do aplicativo).
ms.assetid: 29bf137d-e88b-437f-8bf1-824e335d47a1
title: 'Método ITConnection:: get_BandwidthModifier (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e278edfbdc9ae56d89547c0bcf64f90fde77baf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759472"
---
# <a name="itconnectionget_bandwidthmodifier-method"></a><span data-ttu-id="8a9b7-104">Método ITConnection:: get \_ BandwidthModifier</span><span class="sxs-lookup"><span data-stu-id="8a9b7-104">ITConnection::get\_BandwidthModifier method</span></span>

<span data-ttu-id="8a9b7-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8a9b7-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8a9b7-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="8a9b7-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8a9b7-107">O método **Get \_ BandwidthModifier** Obtém o modificador de largura de banda, que é uma única palavra alfanumérica fornecendo o significado da figura de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="8a9b7-107">The **get\_BandwidthModifier** method gets the bandwidth modifier, which is a single, alphanumeric word giving the meaning of the bandwidth figure.</span></span> <span data-ttu-id="8a9b7-108">Os dois modificadores definidos são CT (total da conferência) e AS (máximo específico do aplicativo).</span><span class="sxs-lookup"><span data-stu-id="8a9b7-108">The two modifiers defined are CT (Conference Total) and AS (Application Specific Maximum).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a9b7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a9b7-109">Syntax</span></span>


```C++
HRESULT get_BandwidthModifier(
  [out] BSTR *ppModifier
);
```



## <a name="parameters"></a><span data-ttu-id="8a9b7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a9b7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a9b7-111">*ppModifier* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8a9b7-111">*ppModifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a9b7-112">Ponteiro para um **BSTR** que contém o modificador de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="8a9b7-112">Pointer to a **BSTR** containing the bandwidth modifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a9b7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a9b7-113">Return value</span></span>

<span data-ttu-id="8a9b7-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8a9b7-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8a9b7-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8a9b7-115">Return code</span></span>                                                                                   | <span data-ttu-id="8a9b7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a9b7-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8a9b7-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a9b7-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8a9b7-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8a9b7-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8a9b7-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="8a9b7-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8a9b7-120">O parâmetro *ppModifier* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="8a9b7-120">The *ppModifier* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="8a9b7-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8a9b7-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8a9b7-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="8a9b7-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8a9b7-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="8a9b7-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8a9b7-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8a9b7-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8a9b7-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8a9b7-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8a9b7-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="8a9b7-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="8a9b7-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a9b7-127">Remarks</span></span>

<span data-ttu-id="8a9b7-128">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppModifier* .</span><span class="sxs-lookup"><span data-stu-id="8a9b7-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppModifier* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a9b7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a9b7-129">Requirements</span></span>



| <span data-ttu-id="8a9b7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a9b7-130">Requirement</span></span> | <span data-ttu-id="8a9b7-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8a9b7-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a9b7-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="8a9b7-132">TAPI version</span></span><br/> | <span data-ttu-id="8a9b7-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8a9b7-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8a9b7-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a9b7-134">Header</span></span><br/>       | <dl> <span data-ttu-id="8a9b7-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a9b7-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a9b7-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a9b7-136">Library</span></span><br/>      | <dl> <span data-ttu-id="8a9b7-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a9b7-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8a9b7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8a9b7-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="8a9b7-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a9b7-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a9b7-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a9b7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a9b7-141">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="8a9b7-141">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

