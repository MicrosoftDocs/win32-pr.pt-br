---
description: O método GetEncryptionKey Obtém a chave de criptografia.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'Método ITConnection:: GetEncryptionKey (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a826dc8424222587f2838804ec035fb23c2e41d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813063"
---
# <a name="itconnectiongetencryptionkey-method"></a><span data-ttu-id="b6995-103">Método ITConnection:: GetEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b6995-103">ITConnection::GetEncryptionKey method</span></span>

<span data-ttu-id="b6995-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b6995-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b6995-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b6995-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b6995-106">O método **GetEncryptionKey** Obtém a chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b6995-106">The **GetEncryptionKey** method gets the encryption key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6995-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6995-107">Syntax</span></span>


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="b6995-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6995-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6995-109">*ppKeyType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b6995-109">*ppKeyType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6995-110">Ponteiro para um **BSTR** que contém o tipo de chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b6995-110">Pointer to a **BSTR** containing the type of encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="b6995-111">*pfValidKeyData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b6995-111">*pfValidKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6995-112">Indica a validade dos dados de chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b6995-112">Indicates validity of encryption key data.</span></span>

</dd> <dt>

<span data-ttu-id="b6995-113">*ppKeyData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b6995-113">*ppKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6995-114">Ponteiro para um **BSTR** que contém os dados da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b6995-114">Pointer to a **BSTR** containing the encryption key data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6995-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6995-115">Return value</span></span>

<span data-ttu-id="b6995-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b6995-116">This method can return one of these values.</span></span>



| <span data-ttu-id="b6995-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b6995-117">Return code</span></span>                                                                                   | <span data-ttu-id="b6995-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6995-118">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6995-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b6995-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b6995-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b6995-120">Method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="b6995-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b6995-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b6995-122">O parâmetro *ppKeyType, pfValidKeyData* ou *ppKeyData* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="b6995-122">The *ppKeyType, pfValidKeyData,* or *ppKeyData* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="b6995-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b6995-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b6995-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="b6995-124">Insufficient memory exists to perform the operation.</span></span><br/>                              |
| <dl> <span data-ttu-id="b6995-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="b6995-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b6995-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="b6995-126">Unspecified error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="b6995-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b6995-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b6995-128">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="b6995-128">This method is not yet implemented.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="b6995-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6995-129">Remarks</span></span>

<span data-ttu-id="b6995-130">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para os parâmetros *ppKeyType* e *ppKeyData* .</span><span class="sxs-lookup"><span data-stu-id="b6995-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppKeyType* and *ppKeyData* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6995-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6995-131">Requirements</span></span>



| <span data-ttu-id="b6995-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6995-132">Requirement</span></span> | <span data-ttu-id="b6995-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b6995-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6995-134">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b6995-134">TAPI version</span></span><br/> | <span data-ttu-id="b6995-135">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b6995-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b6995-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6995-136">Header</span></span><br/>       | <dl> <span data-ttu-id="b6995-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6995-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6995-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6995-138">Library</span></span><br/>      | <dl> <span data-ttu-id="b6995-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6995-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b6995-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b6995-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="b6995-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6995-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6995-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6995-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6995-143">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="b6995-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

