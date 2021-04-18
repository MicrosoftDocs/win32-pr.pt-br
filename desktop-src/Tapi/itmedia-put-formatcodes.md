---
description: O \_ método Put FormatCodes define a lista de códigos de formato de carga de mídia. A variante contém um SAFEARRAY de BSTRs. Cada BSTR dentro dessa matriz é uma cadeia de caracteres de código de formato.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: 'ITMedia: método de ut_FormatCodes de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760342"
---
# <a name="itmediaput_formatcodes-method"></a><span data-ttu-id="a8256-105">ITMedia: método UT \_ FormatCodes:p</span><span class="sxs-lookup"><span data-stu-id="a8256-105">ITMedia::put\_FormatCodes method</span></span>

<span data-ttu-id="a8256-106">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a8256-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a8256-107">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a8256-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a8256-108">O método **Put \_ FormatCodes** define a lista de códigos de formato de carga de mídia.</span><span class="sxs-lookup"><span data-stu-id="a8256-108">The **put\_FormatCodes** method sets the list of media payload format codes.</span></span> <span data-ttu-id="a8256-109">A variante contém um SAFEARRAY de **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="a8256-109">The variant contains a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="a8256-110">Cada **BSTR** dentro dessa matriz é uma cadeia de caracteres de código de formato.</span><span class="sxs-lookup"><span data-stu-id="a8256-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8256-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8256-111">Syntax</span></span>


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a><span data-ttu-id="a8256-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8256-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8256-113">*NEWVAL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8256-113">*NewVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8256-114">Lista de códigos de formato de carga de mídia.</span><span class="sxs-lookup"><span data-stu-id="a8256-114">List of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8256-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8256-115">Return value</span></span>

<span data-ttu-id="a8256-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a8256-116">This method can return one of these values.</span></span>



| <span data-ttu-id="a8256-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a8256-117">Return code</span></span>                                                                                   | <span data-ttu-id="a8256-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8256-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a8256-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a8256-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a8256-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a8256-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a8256-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a8256-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a8256-122">O parâmetro *NEWVAL* não é válido.</span><span class="sxs-lookup"><span data-stu-id="a8256-122">The *NewVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="a8256-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a8256-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a8256-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a8256-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a8256-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="a8256-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a8256-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="a8256-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a8256-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a8256-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a8256-128">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="a8256-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a8256-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8256-129">Remarks</span></span>

<span data-ttu-id="a8256-130">Quando uma lista de formatos de carga é fornecida, isso implica que todos esses formatos podem ser usados na sessão, mas o primeiro desses formatos é o formato padrão para a sessão.</span><span class="sxs-lookup"><span data-stu-id="a8256-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="a8256-131">Quando o protocolo de transporte é RTP, os códigos de formato são tipos de carga RTP.</span><span class="sxs-lookup"><span data-stu-id="a8256-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8256-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8256-132">Requirements</span></span>



| <span data-ttu-id="a8256-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8256-133">Requirement</span></span> | <span data-ttu-id="a8256-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a8256-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8256-135">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a8256-135">TAPI version</span></span><br/> | <span data-ttu-id="a8256-136">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a8256-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a8256-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8256-137">Header</span></span><br/>       | <dl> <span data-ttu-id="a8256-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8256-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8256-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8256-139">Library</span></span><br/>      | <dl> <span data-ttu-id="a8256-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8256-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a8256-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a8256-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="a8256-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8256-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8256-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8256-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8256-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="a8256-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="a8256-145">**ITMedia:: obter \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="a8256-145">**ITMedia::get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




