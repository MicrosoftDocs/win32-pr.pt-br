---
description: O \_ método Put MediaName define o nome da mídia. As mídias definidas são áudio, vídeo, quadro de comunicações, texto e dados.
ms.assetid: 0dd18add-6c7e-40a8-8b39-10c65bdfb2e0
title: 'ITMedia: método de ut_MediaName de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dcbd4e29f59694d610fb4e6af9fd49aa53323d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766224"
---
# <a name="itmediaput_medianame-method"></a><span data-ttu-id="b89a7-104">Método ITMedia::p UT \_ MediaName</span><span class="sxs-lookup"><span data-stu-id="b89a7-104">ITMedia::put\_MediaName method</span></span>

<span data-ttu-id="b89a7-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b89a7-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b89a7-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b89a7-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b89a7-107">O método **Put \_ MediaName** define o nome da mídia.</span><span class="sxs-lookup"><span data-stu-id="b89a7-107">The **put\_MediaName** method sets the media name.</span></span> <span data-ttu-id="b89a7-108">As mídias definidas são áudio, vídeo, quadro de comunicações, texto e dados.</span><span class="sxs-lookup"><span data-stu-id="b89a7-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b89a7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b89a7-109">Syntax</span></span>


```C++
HRESULT put_MediaName(
  [in] BSTR pMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="b89a7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b89a7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b89a7-111">*pMediaName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b89a7-111">*pMediaName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b89a7-112">Ponteiro para um **BSTR** que contém o nome da mídia a ser definido.</span><span class="sxs-lookup"><span data-stu-id="b89a7-112">Pointer to a **BSTR** containing the media name to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b89a7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b89a7-113">Return value</span></span>

<span data-ttu-id="b89a7-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b89a7-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b89a7-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b89a7-115">Return code</span></span>                                                                                   | <span data-ttu-id="b89a7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b89a7-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b89a7-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b89a7-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b89a7-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b89a7-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b89a7-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b89a7-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b89a7-120">O parâmetro *pMediaName* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="b89a7-120">The *pMediaName* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="b89a7-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b89a7-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b89a7-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="b89a7-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b89a7-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="b89a7-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b89a7-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="b89a7-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b89a7-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b89a7-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b89a7-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="b89a7-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b89a7-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="b89a7-127">Remarks</span></span>

<span data-ttu-id="b89a7-128">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PMediaName* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="b89a7-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaName* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="b89a7-129">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="b89a7-129">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="b89a7-130">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="b89a7-130">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b89a7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b89a7-131">Requirements</span></span>



| <span data-ttu-id="b89a7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b89a7-132">Requirement</span></span> | <span data-ttu-id="b89a7-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b89a7-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b89a7-134">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b89a7-134">TAPI version</span></span><br/> | <span data-ttu-id="b89a7-135">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b89a7-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b89a7-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b89a7-136">Header</span></span><br/>       | <dl> <span data-ttu-id="b89a7-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b89a7-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b89a7-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b89a7-138">Library</span></span><br/>      | <dl> <span data-ttu-id="b89a7-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b89a7-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b89a7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b89a7-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="b89a7-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b89a7-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b89a7-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="b89a7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b89a7-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="b89a7-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="b89a7-144">**ITMedia:: obter \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="b89a7-144">**ITMedia::get\_MediaName**</span></span>](itmedia-get-medianame.md)
</dt> </dl>

 

