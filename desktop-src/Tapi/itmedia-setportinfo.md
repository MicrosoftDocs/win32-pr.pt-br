---
description: O método SetPortInfo define o valor da porta de 16 bits para a primeira porta e o número de portas necessárias para uma sessão.
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: 'Método ITMedia:: SetPortInfo (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c605c1768316871f6c3c9ec10f991f21c1643794
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792622"
---
# <a name="itmediasetportinfo-method"></a><span data-ttu-id="fa075-103">Método ITMedia:: SetPortInfo</span><span class="sxs-lookup"><span data-stu-id="fa075-103">ITMedia::SetPortInfo method</span></span>

<span data-ttu-id="fa075-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fa075-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fa075-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="fa075-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fa075-106">O método **SetPortInfo** define o valor da porta de 16 bits para a primeira porta e o número de portas necessárias para uma sessão.</span><span class="sxs-lookup"><span data-stu-id="fa075-106">The **SetPortInfo** method sets the 16-bit port value for the first port and the number of ports needed for a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa075-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa075-107">Syntax</span></span>


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="fa075-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa075-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa075-109">*StartPort* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa075-109">*StartPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa075-110">Porta inicial.</span><span class="sxs-lookup"><span data-stu-id="fa075-110">Starting port.</span></span> <span data-ttu-id="fa075-111">Isso pode ser um valor no intervalo de 0-65535.</span><span class="sxs-lookup"><span data-stu-id="fa075-111">This can be a value in the range 0-65535.</span></span>

</dd> <dt>

<span data-ttu-id="fa075-112">*NumPorts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa075-112">*NumPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa075-113">Número de portas.</span><span class="sxs-lookup"><span data-stu-id="fa075-113">Number of ports.</span></span> <span data-ttu-id="fa075-114">Isso pode ser um valor no intervalo de 0-65535.</span><span class="sxs-lookup"><span data-stu-id="fa075-114">This can be a value in the range 0-65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa075-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa075-115">Return value</span></span>

<span data-ttu-id="fa075-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="fa075-116">This method can return one of these values.</span></span>



| <span data-ttu-id="fa075-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fa075-117">Return code</span></span>                                                                                   | <span data-ttu-id="fa075-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa075-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fa075-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa075-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fa075-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fa075-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fa075-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fa075-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fa075-122">O parâmetro *StartPort ou NumPorts* não é válido.</span><span class="sxs-lookup"><span data-stu-id="fa075-122">The *StartPort or NumPorts* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="fa075-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fa075-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fa075-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="fa075-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fa075-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="fa075-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fa075-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="fa075-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fa075-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="fa075-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fa075-128">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="fa075-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="fa075-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa075-129">Remarks</span></span>

<span data-ttu-id="fa075-130">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="fa075-130">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="fa075-131">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="fa075-131">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa075-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa075-132">Requirements</span></span>



| <span data-ttu-id="fa075-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa075-133">Requirement</span></span> | <span data-ttu-id="fa075-134">Valor</span><span class="sxs-lookup"><span data-stu-id="fa075-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa075-135">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="fa075-135">TAPI version</span></span><br/> | <span data-ttu-id="fa075-136">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="fa075-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fa075-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa075-137">Header</span></span><br/>       | <dl> <span data-ttu-id="fa075-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa075-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa075-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa075-139">Library</span></span><br/>      | <dl> <span data-ttu-id="fa075-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa075-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fa075-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fa075-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="fa075-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa075-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa075-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa075-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa075-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="fa075-144">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




