---
title: Função MpErrorMessageFormat (MpClient. h)
description: Retorna uma mensagem de erro formatada com base em um código de erro.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Recursos do ambiente Windows herdado da função MpErrorMessageFormat
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a3499b3be885b29135d22b470da4143cfb23ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919026"
---
# <a name="mperrormessageformat-function"></a><span data-ttu-id="f9c58-104">Função MpErrorMessageFormat</span><span class="sxs-lookup"><span data-stu-id="f9c58-104">MpErrorMessageFormat function</span></span>

<span data-ttu-id="f9c58-105">Retorna uma mensagem de erro formatada com base em um código de erro.</span><span class="sxs-lookup"><span data-stu-id="f9c58-105">Returns a formatted error message based on an error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c58-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9c58-106">Syntax</span></span>


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a><span data-ttu-id="f9c58-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9c58-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9c58-108">*hMpHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9c58-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c58-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="f9c58-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="f9c58-110">Identificador para a interface do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="f9c58-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="f9c58-111">Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="f9c58-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f9c58-112">*hrError* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9c58-112">*hrError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c58-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f9c58-113">Type: **HRESULT**</span></span>

<span data-ttu-id="f9c58-114">Um código de erro com base em **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f9c58-114">An **HRESULT**-based error code.</span></span>

</dd> <dt>

<span data-ttu-id="f9c58-115">*pwszErrorDesc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f9c58-115">*pwszErrorDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c58-116">Tipo: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="f9c58-116">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="f9c58-117">Retorna uma mensagem de erro formatada com base em _hrError \*.</span><span class="sxs-lookup"><span data-stu-id="f9c58-117">Returns a formatted error message based on _hrError\*.</span></span> <span data-ttu-id="f9c58-118">Essa cadeia de caracteres deve ser liberada usando [**MpFreeMemory**](mpfreememory.md).</span><span class="sxs-lookup"><span data-stu-id="f9c58-118">This string must be freed using [**MpFreeMemory**](mpfreememory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9c58-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9c58-119">Return value</span></span>

<span data-ttu-id="f9c58-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f9c58-120">Type: **HRESULT**</span></span>

<span data-ttu-id="f9c58-121">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f9c58-121">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="f9c58-122">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="f9c58-122">If the function fails then the return value is a failed **HRESULT** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9c58-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9c58-123">Remarks</span></span>

<span data-ttu-id="f9c58-124">Essa função é capaz de Formatar códigos de erro do sistema, além de códigos de erro específicos retornados pelas funções de proteção contra malware.</span><span class="sxs-lookup"><span data-stu-id="f9c58-124">This function is capable of formatting system error codes in addition to specific error codes returned by malware protection functions.</span></span> <span data-ttu-id="f9c58-125">Os códigos de erro **HRESULT** específicos das funções de proteção contra malware têm uma facilidade de 0x50.</span><span class="sxs-lookup"><span data-stu-id="f9c58-125">The **HRESULT** error codes specific to malware protection functions have a facility of 0x50.</span></span> <span data-ttu-id="f9c58-126">Abaixo está uma lista de um subconjunto dos códigos de erro específicos da proteção contra malware que podem ser retornados por várias funções de proteção contra malware.</span><span class="sxs-lookup"><span data-stu-id="f9c58-126">Below is a list of a subset of the malware protection-specific error codes that can be returned by various malware protection functions.</span></span> <span data-ttu-id="f9c58-127">Usando a macro **HRESULT \_ do \_ \_ status do MP**, os códigos de erro a seguir podem ser convertidos em **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f9c58-127">Using the macro **HRESULT\_FROM\_MP\_STATUS**, the following error codes can be converted to **HRESULT**.</span></span> <span data-ttu-id="f9c58-128">Consulte também [códigos de erro do mecanismo anti-malware do Forefront Client Security](https://support.microsoft.com/kb/939359) para obter uma lista de outros códigos de erro possíveis.</span><span class="sxs-lookup"><span data-stu-id="f9c58-128">See also [Forefront Client Security anti-malware engine error codes](https://support.microsoft.com/kb/939359) for a list of other possible error codes.</span></span>



| <span data-ttu-id="f9c58-129">Código do Erro</span><span class="sxs-lookup"><span data-stu-id="f9c58-129">Error Code</span></span>                              | <span data-ttu-id="f9c58-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9c58-130">Description</span></span>                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c58-131">ERRO \_ MP \_ noengine</span><span class="sxs-lookup"><span data-stu-id="f9c58-131">ERROR\_MP\_NOENGINE</span></span>                     | <span data-ttu-id="f9c58-132">Nenhum mecanismo é carregado no serviço antimalware para executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="f9c58-132">No engine is loaded in antimalware service to perform the requested operation.</span></span>                                              |
| <span data-ttu-id="f9c58-133">ERRO \_ MP \_ sem \_ memória</span><span class="sxs-lookup"><span data-stu-id="f9c58-133">ERROR\_MP\_NO\_MEMORY</span></span>                   | <span data-ttu-id="f9c58-134">O mecanismo Antimalware encontrou uma situação sem memória.</span><span class="sxs-lookup"><span data-stu-id="f9c58-134">The antimalware engine has encountered a no memory situation.</span></span>                                                               |
| <span data-ttu-id="f9c58-135">ERRO \_ \_ ao remover MP \_ com falha</span><span class="sxs-lookup"><span data-stu-id="f9c58-135">ERROR\_MP\_REMOVE\_FAILED</span></span>               | <span data-ttu-id="f9c58-136">Falha na operação de remoção de uma ameaça específica.</span><span class="sxs-lookup"><span data-stu-id="f9c58-136">Remove operation failed for a specific threat.</span></span>                                                                              |
| <span data-ttu-id="f9c58-137">\_ \_ falha na quarentena do MP de erro \_</span><span class="sxs-lookup"><span data-stu-id="f9c58-137">ERROR\_MP\_QUARANTINE\_FAILED</span></span>           | <span data-ttu-id="f9c58-138">Falha na operação de quarentena para uma ameaça específica.</span><span class="sxs-lookup"><span data-stu-id="f9c58-138">Quarantine operation failed for a specific threat.</span></span>                                                                          |
| <span data-ttu-id="f9c58-139">ERRO \_ de \_ ameaça de MP \_ não \_ encontrada</span><span class="sxs-lookup"><span data-stu-id="f9c58-139">ERROR\_MP\_THREAT\_NOT\_FOUND</span></span>           | <span data-ttu-id="f9c58-140">A ameaça específica não existe mais no sistema.</span><span class="sxs-lookup"><span data-stu-id="f9c58-140">The specific threat no longer exists in the system.</span></span>                                                                         |
| <span data-ttu-id="f9c58-141">ERRO \_ de \_ remoção de MP \_ sem \_ suporte</span><span class="sxs-lookup"><span data-stu-id="f9c58-141">ERROR\_MP\_REMOVE\_NOT\_SUPPORTED</span></span>       | <span data-ttu-id="f9c58-142">Não há suporte para a operação de remoção de uma ameaça específica dentro do tipo de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f9c58-142">Remove operation for a specific threat inside the container type is not supported.</span></span>                                          |
| <span data-ttu-id="f9c58-143">ERRO \_ MP \_ Remover \_ contêiner imutável \_</span><span class="sxs-lookup"><span data-stu-id="f9c58-143">ERROR\_MP\_REMOVE\_IMMUTABLE\_CONTAINER</span></span> | <span data-ttu-id="f9c58-144">Devido à política do mecanismo, não há suporte para uma operação de remoção de uma ameaça específica dentro de um contêiner bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f9c58-144">Due to engine policy, a remove operation of a specific threat inside a blocked container is not supported.</span></span> <span data-ttu-id="f9c58-145">(Arquivos mortos de email).</span><span class="sxs-lookup"><span data-stu-id="f9c58-145">(Mail archives.)</span></span> |
| <span data-ttu-id="f9c58-146">ERRO \_ MP \_ BADDB \_ OLDENGINE</span><span class="sxs-lookup"><span data-stu-id="f9c58-146">ERROR\_MP\_BADDB\_OLDENGINE</span></span>             | <span data-ttu-id="f9c58-147">A solicitação de atualização de assinatura forneceu arquivos de assinatura ou mecanismo mais antigos.</span><span class="sxs-lookup"><span data-stu-id="f9c58-147">Signature update request provided an older engine or signature files(s).</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="f9c58-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9c58-148">Requirements</span></span>



| <span data-ttu-id="f9c58-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9c58-149">Requirement</span></span> | <span data-ttu-id="f9c58-150">Valor</span><span class="sxs-lookup"><span data-stu-id="f9c58-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c58-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9c58-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c58-152">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f9c58-152">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f9c58-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9c58-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c58-154">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f9c58-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9c58-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9c58-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9c58-156"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9c58-156"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9c58-157">DLL</span><span class="sxs-lookup"><span data-stu-id="f9c58-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9c58-158"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9c58-158"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9c58-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9c58-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c58-160">**MpFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="f9c58-160">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="f9c58-161">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="f9c58-161">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="f9c58-162">Códigos de erro do mecanismo anti-malware do Forefront Client Security</span><span class="sxs-lookup"><span data-stu-id="f9c58-162">Forefront Client Security anti-malware engine error codes</span></span>](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





