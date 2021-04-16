---
description: O método SetBandwidthInfo define as informações de largura de banda.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'Método ITConnection:: SetBandwidthInfo (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779905"
---
# <a name="itconnectionsetbandwidthinfo-method"></a><span data-ttu-id="4e6fc-103">Método ITConnection:: SetBandwidthInfo</span><span class="sxs-lookup"><span data-stu-id="4e6fc-103">ITConnection::SetBandwidthInfo method</span></span>

<span data-ttu-id="4e6fc-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4e6fc-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4e6fc-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4e6fc-106">O método **SetBandwidthInfo** define as informações de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-106">The **SetBandwidthInfo** method sets the bandwidth information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e6fc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e6fc-107">Syntax</span></span>


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="4e6fc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e6fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e6fc-109">*pModifier* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e6fc-109">*pModifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e6fc-110">Ponteiro para um **BSTR** que indica o escopo da largura de banda que está sendo definida.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-110">Pointer to a **BSTR** indicating the scope of the bandwidth being set.</span></span> <span data-ttu-id="4e6fc-111">Para obter mais informações, consulte a seção Comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-111">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="4e6fc-112">*Largura de banda* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e6fc-112">*Bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e6fc-113">Larga.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-113">Bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e6fc-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e6fc-114">Return value</span></span>

<span data-ttu-id="4e6fc-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4e6fc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4e6fc-116">Value</span></span>                                                                                         | <span data-ttu-id="4e6fc-117">Significado</span><span class="sxs-lookup"><span data-stu-id="4e6fc-117">Meaning</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="4e6fc-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4e6fc-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4e6fc-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-119">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="4e6fc-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4e6fc-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4e6fc-121">O parâmetro *pModifier* ou *Bandwidth* não é válido.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-121">The *pModifier* or *Bandwidth* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="4e6fc-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4e6fc-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4e6fc-123">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-123">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="4e6fc-124"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="4e6fc-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4e6fc-125">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-125">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4e6fc-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4e6fc-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4e6fc-127">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-127">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="4e6fc-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e6fc-128">Remarks</span></span>

<span data-ttu-id="4e6fc-129">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PModifier* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-129">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pModifier* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="4e6fc-130">Referência: RFC 2327.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-130">Reference: RFC 2327.</span></span>

<span data-ttu-id="4e6fc-131">O modificador de largura de banda normalmente será o CT ou como:</span><span class="sxs-lookup"><span data-stu-id="4e6fc-131">The bandwidth modifier will normally be either CT or AS:</span></span>

<span data-ttu-id="4e6fc-132">**Total da conferência CT:** Uma largura de banda máxima implícita é associada [*a cada TTL*](t-tapgloss.md) (vida útil) no MBone ou dentro de uma região de escopo administrativo de multicast específica (a largura de banda MBone versus os limites de TTL são fornecidos nas perguntas frequentes sobre o MBone).</span><span class="sxs-lookup"><span data-stu-id="4e6fc-132">**CT Conference Total:** An implicit maximum bandwidth is associated with each [*time to live*](t-tapgloss.md) (TTL) on the Mbone or within a particular multicast administrative scope region (the Mbone bandwidth versus TTL limits are given in the MBone FAQ).</span></span> <span data-ttu-id="4e6fc-133">Se a largura de banda de uma sessão ou mídia em uma sessão for diferente da largura de banda implícita do escopo, a \` b = CT:... ' a linha deve ser fornecida para a sessão, fornecendo o limite superior proposto à largura de banda usada.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-133">If the bandwidth of a session or media in a session is different from the bandwidth implicit from the scope, a \`b=CT:...' line should be supplied for the session giving the proposed upper limit to the bandwidth used.</span></span> <span data-ttu-id="4e6fc-134">A principal finalidade disso é dar uma ideia aproximada de se duas ou mais conferências podem coexistir simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-134">The primary purpose of this is to give an approximate idea as to whether two or more conferences can coexist simultaneously.</span></span>

<span data-ttu-id="4e6fc-135">**Máximo de Application-Specific:** A largura de banda é interpretada para ser específica ao aplicativo, ou seja, será o conceito de largura de banda máxima do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-135">**AS Application-Specific Maximum:** The bandwidth is interpreted to be application-specific, i.e., will be the application's concept of maximum bandwidth.</span></span> <span data-ttu-id="4e6fc-136">Normalmente, isso coincidirá com o que está definido no controle "máximo de largura de banda" do aplicativo, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-136">Normally this will coincide with what is set on the application's "maximum bandwidth" control, if applicable.</span></span>

<span data-ttu-id="4e6fc-137">Observe que a CT fornece uma figura de largura de banda total para todas as mídias em todos os sites.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-137">Note that CT gives a total bandwidth figure for all the media at all sites.</span></span> <span data-ttu-id="4e6fc-138">COMO o fornece uma figura de largura de banda para uma única mídia em um único site, embora possa haver muitos sites enviando simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="4e6fc-138">AS gives a bandwidth figure for a single media at a single site, although there may be many sites sending simultaneously.</span></span>

<span data-ttu-id="4e6fc-139">**Mecanismo de extensão:** Os escritores de ferramenta podem definir modificadores de largura de banda experimentais prefixando seus modificadores com "X-".</span><span class="sxs-lookup"><span data-stu-id="4e6fc-139">**Extension Mechanism:** Tool writers can define experimental bandwidth modifiers by prefixing their modifiers with "X-".</span></span>

## <a name="requirements"></a><span data-ttu-id="4e6fc-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e6fc-140">Requirements</span></span>



| <span data-ttu-id="4e6fc-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e6fc-141">Requirement</span></span> | <span data-ttu-id="4e6fc-142">Valor</span><span class="sxs-lookup"><span data-stu-id="4e6fc-142">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e6fc-143">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="4e6fc-143">TAPI version</span></span><br/> | <span data-ttu-id="4e6fc-144">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4e6fc-144">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4e6fc-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e6fc-145">Header</span></span><br/>       | <dl> <span data-ttu-id="4e6fc-146"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e6fc-146"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e6fc-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e6fc-147">Library</span></span><br/>      | <dl> <span data-ttu-id="4e6fc-148"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e6fc-148"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4e6fc-149">DLL</span><span class="sxs-lookup"><span data-stu-id="4e6fc-149">DLL</span></span><br/>          | <dl> <span data-ttu-id="4e6fc-150"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e6fc-150"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e6fc-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e6fc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e6fc-152">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="4e6fc-152">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

