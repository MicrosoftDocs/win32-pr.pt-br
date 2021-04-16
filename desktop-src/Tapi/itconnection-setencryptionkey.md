---
description: O método SetEncryptionKey define a chave de criptografia necessária para descriptografar a sessão ou uma indicação para um mecanismo para obter uma chave utilizável por meios externos.
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'Método ITConnection:: SetEncryptionKey (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d0ce079d3815897c348e553df0af8dece8592b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757966"
---
# <a name="itconnectionsetencryptionkey-method"></a><span data-ttu-id="95446-103">Método ITConnection:: SetEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="95446-103">ITConnection::SetEncryptionKey method</span></span>

<span data-ttu-id="95446-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="95446-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="95446-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="95446-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="95446-106">O método **SetEncryptionKey** define a chave de criptografia necessária para descriptografar a sessão ou uma indicação para um mecanismo para obter uma chave utilizável por meios externos.</span><span class="sxs-lookup"><span data-stu-id="95446-106">The **SetEncryptionKey** method sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span>

## <a name="syntax"></a><span data-ttu-id="95446-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95446-107">Syntax</span></span>


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="95446-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95446-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95446-109">*pKeyType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95446-109">*pKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95446-110">Ponteiro para um **BSTR** que contém o tipo de chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="95446-110">Pointer to a **BSTR** containing the encryption key type.</span></span>

</dd> <dt>

<span data-ttu-id="95446-111">*ppKeyData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95446-111">*ppKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95446-112">Ponteiro para um **BSTR** contendo informações de chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="95446-112">Pointer to a **BSTR** containing encryption key information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95446-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95446-113">Return value</span></span>

<span data-ttu-id="95446-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="95446-114">This method can return one of these values.</span></span>



| <span data-ttu-id="95446-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="95446-115">Return code</span></span>                                                                          | <span data-ttu-id="95446-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="95446-116">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="95446-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="95446-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="95446-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="95446-118">Method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95446-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="95446-119">Remarks</span></span>

<span data-ttu-id="95446-120">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para os parâmetros *pKeyType* e *ppKeyData* .</span><span class="sxs-lookup"><span data-stu-id="95446-120">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pKeyType* and *ppKeyData* parameters.</span></span> <span data-ttu-id="95446-121">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando as variáveis não forem mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="95446-121">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="95446-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95446-122">Requirements</span></span>



| <span data-ttu-id="95446-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="95446-123">Requirement</span></span> | <span data-ttu-id="95446-124">Valor</span><span class="sxs-lookup"><span data-stu-id="95446-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95446-125">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="95446-125">TAPI version</span></span><br/> | <span data-ttu-id="95446-126">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="95446-126">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="95446-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95446-127">Header</span></span><br/>       | <dl> <span data-ttu-id="95446-128"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="95446-128"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="95446-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95446-129">Library</span></span><br/>      | <dl> <span data-ttu-id="95446-130"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95446-130"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="95446-131">DLL</span><span class="sxs-lookup"><span data-stu-id="95446-131">DLL</span></span><br/>          | <dl> <span data-ttu-id="95446-132"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95446-132"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95446-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="95446-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95446-134">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="95446-134">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

