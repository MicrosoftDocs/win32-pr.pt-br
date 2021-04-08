---
description: O método getchallenge constrói um comando APDU (unidade de dados do protocolo de aplicativo) que emite um desafio (por exemplo, um número aleatório) para uso em um procedimento relacionado à segurança.
ms.assetid: 61f6db1c-b83a-4c1f-8ace-0222a12560ff
title: 'Método ISCardISO7816:: getchallenge (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetChallenge
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 05fe18ad73de6c7c3ea30f986c7bb3420bc465b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011458"
---
# <a name="iscardiso7816getchallenge-method"></a><span data-ttu-id="99e66-103">Método ISCardISO7816:: getchallenge</span><span class="sxs-lookup"><span data-stu-id="99e66-103">ISCardISO7816::GetChallenge method</span></span>

<span data-ttu-id="99e66-104">\[O método **getchallenge** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="99e66-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="99e66-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="99e66-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="99e66-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="99e66-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="99e66-107">O método **getchallenge** constrói um comando APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ) que emite um desafio (por exemplo, um número aleatório) para uso em um procedimento relacionado à segurança.</span><span class="sxs-lookup"><span data-stu-id="99e66-107">The **GetChallenge** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that issue a challenge (for example, a random number) for use in a security-related procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e66-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99e66-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in]      LONG       lBytesExpected,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="99e66-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99e66-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99e66-110">*lBytesExpected* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99e66-110">*lBytesExpected* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e66-111">Comprimento máximo da resposta esperada.</span><span class="sxs-lookup"><span data-stu-id="99e66-111">Maximum length of the expected response.</span></span>

</dd> <dt>

<span data-ttu-id="99e66-112">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="99e66-112">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99e66-113">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="99e66-113">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="99e66-114">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="99e66-114">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="99e66-115">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado por meio do ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="99e66-115">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99e66-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99e66-116">Return value</span></span>

<span data-ttu-id="99e66-117">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="99e66-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="99e66-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="99e66-118">Return code</span></span>                                                                                   | <span data-ttu-id="99e66-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="99e66-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="99e66-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="99e66-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="99e66-121">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="99e66-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="99e66-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="99e66-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="99e66-123">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="99e66-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="99e66-124"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="99e66-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="99e66-125">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="99e66-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="99e66-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="99e66-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="99e66-127">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="99e66-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="99e66-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="99e66-128">Remarks</span></span>

<span data-ttu-id="99e66-129">O desafio é válido pelo menos para o próximo comando.</span><span class="sxs-lookup"><span data-stu-id="99e66-129">The challenge is valid at least for the next command.</span></span>

<span data-ttu-id="99e66-130">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="99e66-130">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="99e66-131">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="99e66-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="99e66-132">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="99e66-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99e66-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99e66-133">Requirements</span></span>



| <span data-ttu-id="99e66-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="99e66-134">Requirement</span></span> | <span data-ttu-id="99e66-135">Valor</span><span class="sxs-lookup"><span data-stu-id="99e66-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99e66-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99e66-136">Minimum supported client</span></span><br/> | <span data-ttu-id="99e66-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="99e66-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="99e66-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99e66-138">Minimum supported server</span></span><br/> | <span data-ttu-id="99e66-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="99e66-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99e66-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="99e66-140">End of client support</span></span><br/>    | <span data-ttu-id="99e66-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="99e66-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="99e66-142">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="99e66-142">End of server support</span></span><br/>    | <span data-ttu-id="99e66-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99e66-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="99e66-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99e66-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="99e66-145"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="99e66-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="99e66-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="99e66-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="99e66-147"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="99e66-147"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="99e66-148">DLL</span><span class="sxs-lookup"><span data-stu-id="99e66-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99e66-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99e66-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="99e66-150">IID</span><span class="sxs-lookup"><span data-stu-id="99e66-150">IID</span></span><br/>                      | <span data-ttu-id="99e66-151">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="99e66-151">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="99e66-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="99e66-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e66-153">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="99e66-153">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="99e66-154">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="99e66-154">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="99e66-155">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="99e66-155">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
