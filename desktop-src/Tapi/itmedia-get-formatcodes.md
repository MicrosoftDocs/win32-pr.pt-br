---
description: O \_ método Get FormatCodes Obtém a lista de códigos de formato de carga de mídia. A variante retorna um SAFEARRAY de BSTRs. Cada BSTR dentro dessa matriz é uma cadeia de caracteres de código de formato.
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'Método ITMedia:: get_FormatCodes (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9e28a0323ac001c948a3b19b8dae2cfe9daf5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757226"
---
# <a name="itmediaget_formatcodes-method"></a><span data-ttu-id="13a30-105">Método ITMedia:: get \_ FormatCodes</span><span class="sxs-lookup"><span data-stu-id="13a30-105">ITMedia::get\_FormatCodes method</span></span>

<span data-ttu-id="13a30-106">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="13a30-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="13a30-107">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="13a30-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="13a30-108">O método **Get \_ FormatCodes** Obtém a lista de códigos de formato de carga de mídia.</span><span class="sxs-lookup"><span data-stu-id="13a30-108">The **get\_FormatCodes** method gets the list of media payload format codes.</span></span> <span data-ttu-id="13a30-109">A variante retorna um SAFEARRAY de **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="13a30-109">The variant returns a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="13a30-110">Cada **BSTR** dentro dessa matriz é uma cadeia de caracteres de código de formato.</span><span class="sxs-lookup"><span data-stu-id="13a30-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a30-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13a30-111">Syntax</span></span>


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="13a30-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13a30-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a30-113">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="13a30-113">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13a30-114">Matriz de códigos de formato de carga de mídia.</span><span class="sxs-lookup"><span data-stu-id="13a30-114">Array of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a30-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13a30-115">Return value</span></span>

<span data-ttu-id="13a30-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="13a30-116">This method can return one of these values.</span></span>



| <span data-ttu-id="13a30-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="13a30-117">Return code</span></span>                                                                                   | <span data-ttu-id="13a30-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="13a30-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="13a30-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="13a30-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="13a30-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="13a30-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="13a30-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="13a30-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="13a30-122">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="13a30-122">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="13a30-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="13a30-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="13a30-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="13a30-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="13a30-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="13a30-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="13a30-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="13a30-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="13a30-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="13a30-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="13a30-128">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="13a30-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="13a30-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="13a30-129">Remarks</span></span>

<span data-ttu-id="13a30-130">Quando uma lista de formatos de carga é fornecida, isso implica que todos esses formatos podem ser usados na sessão, mas o primeiro desses formatos é o formato padrão para a sessão.</span><span class="sxs-lookup"><span data-stu-id="13a30-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="13a30-131">Quando o protocolo de transporte é RTP, os códigos de formato são tipos de carga RTP.</span><span class="sxs-lookup"><span data-stu-id="13a30-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a30-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13a30-132">Requirements</span></span>



| <span data-ttu-id="13a30-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="13a30-133">Requirement</span></span> | <span data-ttu-id="13a30-134">Valor</span><span class="sxs-lookup"><span data-stu-id="13a30-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13a30-135">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="13a30-135">TAPI version</span></span><br/> | <span data-ttu-id="13a30-136">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="13a30-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="13a30-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="13a30-137">Header</span></span><br/>       | <dl> <span data-ttu-id="13a30-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="13a30-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="13a30-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="13a30-139">Library</span></span><br/>      | <dl> <span data-ttu-id="13a30-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13a30-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="13a30-141">DLL</span><span class="sxs-lookup"><span data-stu-id="13a30-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="13a30-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13a30-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a30-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="13a30-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a30-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="13a30-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="13a30-145">**ITMedia::p UT \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="13a30-145">**ITMedia::put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




