---
description: O método SetConferenceBlob confirma as alterações no blob de conferência. Para inicializar o blob de conferência pela primeira vez, use o método Init em vez disso.
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'Método ITConferenceBlob:: SetConferenceBlob (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47779807e5bde6a070b4600aec903309c7679dc8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769416"
---
# <a name="itconferenceblobsetconferenceblob-method"></a><span data-ttu-id="1d165-104">Método ITConferenceBlob:: SetConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="1d165-104">ITConferenceBlob::SetConferenceBlob method</span></span>

<span data-ttu-id="1d165-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1d165-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1d165-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1d165-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1d165-107">O método **SetConferenceBlob** confirma as alterações no blob de conferência.</span><span class="sxs-lookup"><span data-stu-id="1d165-107">The **SetConferenceBlob** method commits changes to the conference blob.</span></span> <span data-ttu-id="1d165-108">Para inicializar o blob de conferência pela primeira vez, use o método [**init**](itconferenceblob-init.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1d165-108">To initialize the conference blob for the first time, use the [**Init**](itconferenceblob-init.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d165-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d165-109">Syntax</span></span>


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="1d165-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d165-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d165-111">*CharacterSet* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d165-111">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d165-112">[**Blob \_ do \_**](blob-character-set.md) Descritor do conjunto de caracteres do conjunto de caracteres do blob de conferência.</span><span class="sxs-lookup"><span data-stu-id="1d165-112">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the conference blob's character set.</span></span>

</dd> <dt>

<span data-ttu-id="1d165-113">*pBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d165-113">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d165-114">Ponteiro para um **BSTR** que contém o blob de conferência.</span><span class="sxs-lookup"><span data-stu-id="1d165-114">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d165-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d165-115">Return value</span></span>

<span data-ttu-id="1d165-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1d165-116">This method can return one of these values.</span></span>



| <span data-ttu-id="1d165-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1d165-117">Return code</span></span>                                                                                   | <span data-ttu-id="1d165-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d165-118">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d165-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d165-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1d165-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1d165-120">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="1d165-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1d165-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1d165-122">O parâmetro *CharacterSet* ou *pBlob* não é válido.</span><span class="sxs-lookup"><span data-stu-id="1d165-122">The *CharacterSet* or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="1d165-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1d165-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1d165-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1d165-124">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="1d165-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1d165-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1d165-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1d165-126">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1d165-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1d165-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1d165-128">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="1d165-128">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="1d165-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d165-129">Remarks</span></span>

<span data-ttu-id="1d165-130">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PBlob* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="1d165-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pBlob* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d165-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d165-131">Requirements</span></span>



| <span data-ttu-id="1d165-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d165-132">Requirement</span></span> | <span data-ttu-id="1d165-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1d165-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d165-134">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1d165-134">TAPI version</span></span><br/> | <span data-ttu-id="1d165-135">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1d165-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1d165-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d165-136">Header</span></span><br/>       | <dl> <span data-ttu-id="1d165-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d165-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d165-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d165-138">Library</span></span><br/>      | <dl> <span data-ttu-id="1d165-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d165-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1d165-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1d165-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="1d165-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d165-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d165-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d165-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d165-143">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="1d165-143">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="1d165-144">**\_conjunto de caracteres de blob \_**</span><span class="sxs-lookup"><span data-stu-id="1d165-144">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

