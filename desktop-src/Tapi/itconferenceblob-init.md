---
description: O método Init Inicializa o blob de conferência com base em uma cadeia de caracteres textual. Se pBlob for NULL, os valores padrão serão usados.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'Método ITConferenceBlob:: init (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789459"
---
# <a name="itconferenceblobinit-method"></a><span data-ttu-id="48918-104">Método ITConferenceBlob:: init</span><span class="sxs-lookup"><span data-stu-id="48918-104">ITConferenceBlob::Init method</span></span>

<span data-ttu-id="48918-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="48918-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="48918-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="48918-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="48918-107">O método **init** Inicializa o blob de conferência com base em uma cadeia de caracteres textual.</span><span class="sxs-lookup"><span data-stu-id="48918-107">The **Init** method initializes the conference blob based on a textual string.</span></span> <span data-ttu-id="48918-108">Se *pBlob* for **NULL**, os valores padrão serão usados.</span><span class="sxs-lookup"><span data-stu-id="48918-108">If *pBlob* is **NULL**, default values are used.</span></span>

## <a name="syntax"></a><span data-ttu-id="48918-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48918-109">Syntax</span></span>


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="48918-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48918-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48918-111">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48918-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48918-112">Ponteiro para uma representação **BSTR** do nome da conferência.</span><span class="sxs-lookup"><span data-stu-id="48918-112">Pointer to a **BSTR** representation of the conference name.</span></span>

</dd> <dt>

<span data-ttu-id="48918-113">*CharacterSet* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48918-113">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48918-114">[**Blob \_ do \_**](blob-character-set.md) Descritor do conjunto de caracteres do conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="48918-114">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> <dt>

<span data-ttu-id="48918-115">*pBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48918-115">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48918-116">Ponteiro para um **BSTR** que contém o blob de conferência.</span><span class="sxs-lookup"><span data-stu-id="48918-116">Pointer to a **BSTR** containing the conference blob.</span></span> <span data-ttu-id="48918-117">Se for **NULL**, o blob de conferência será inicializado com valores padrão.</span><span class="sxs-lookup"><span data-stu-id="48918-117">If **NULL**, the conference blob is initialized with default values.</span></span> <span data-ttu-id="48918-118">Atualmente, os valores de conferência padrão só estarão disponíveis se o parâmetro *CharacterSet* estiver definido como BCS \_ ASCII.</span><span class="sxs-lookup"><span data-stu-id="48918-118">Currently, default conference values are available only if the *CharacterSet* parameter is set to BCS\_ASCII.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48918-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48918-119">Return value</span></span>

<span data-ttu-id="48918-120">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="48918-120">This method can return one of these values.</span></span>



| <span data-ttu-id="48918-121">Valor</span><span class="sxs-lookup"><span data-stu-id="48918-121">Value</span></span>                                                                                         | <span data-ttu-id="48918-122">Significado</span><span class="sxs-lookup"><span data-stu-id="48918-122">Meaning</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48918-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48918-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="48918-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="48918-124">Method succeeded.</span></span><br/>                                               |
| <dl> <span data-ttu-id="48918-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="48918-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="48918-126">O parâmetro *pname*, *CharacterSet* ou *pBlob* não é válido.</span><span class="sxs-lookup"><span data-stu-id="48918-126">The *pName*, *CharacterSet*, or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="48918-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="48918-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="48918-128">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="48918-128">Insufficient memory exists to perform the operation.</span></span><br/>            |
| <dl> <span data-ttu-id="48918-129"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="48918-129"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="48918-130">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="48918-130">Unspecified error.</span></span><br/>                                              |
| <dl> <span data-ttu-id="48918-131"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="48918-131"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="48918-132">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="48918-132">This method is not yet implemented.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="48918-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="48918-133">Remarks</span></span>

<span data-ttu-id="48918-134">**ITConferenceBlob:: init** retornará uma falha se o blob já tiver sido inicializado.</span><span class="sxs-lookup"><span data-stu-id="48918-134">**ITConferenceBlob::Init** will return a failure if the blob has already been initialized.</span></span>

<span data-ttu-id="48918-135">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para os parâmetros *pname* e *pBlob* .</span><span class="sxs-lookup"><span data-stu-id="48918-135">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pName* and *pBlob* parameters.</span></span> <span data-ttu-id="48918-136">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando as variáveis não forem mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="48918-136">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="48918-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48918-137">Requirements</span></span>



| <span data-ttu-id="48918-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="48918-138">Requirement</span></span> | <span data-ttu-id="48918-139">Valor</span><span class="sxs-lookup"><span data-stu-id="48918-139">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48918-140">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="48918-140">TAPI version</span></span><br/> | <span data-ttu-id="48918-141">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="48918-141">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="48918-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48918-142">Header</span></span><br/>       | <dl> <span data-ttu-id="48918-143"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="48918-143"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="48918-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48918-144">Library</span></span><br/>      | <dl> <span data-ttu-id="48918-145"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48918-145"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="48918-146">DLL</span><span class="sxs-lookup"><span data-stu-id="48918-146">DLL</span></span><br/>          | <dl> <span data-ttu-id="48918-147"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48918-147"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48918-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="48918-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48918-149">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="48918-149">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="48918-150">**\_conjunto de caracteres de blob \_**</span><span class="sxs-lookup"><span data-stu-id="48918-150">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

