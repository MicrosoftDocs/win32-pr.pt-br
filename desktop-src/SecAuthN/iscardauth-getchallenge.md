---
description: O método getchallenge retorna um desafio do cartão inteligente.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: 'Método ISCardAuth:: getchallenge'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9282c0a922a1f8c8daff07c31dcafa7e47e923a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164986"
---
# <a name="iscardauthgetchallenge-method"></a><span data-ttu-id="50e53-103">Método ISCardAuth:: getchallenge</span><span class="sxs-lookup"><span data-stu-id="50e53-103">ISCardAuth::GetChallenge method</span></span>

<span data-ttu-id="50e53-104">\[O método **getchallenge** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="50e53-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="50e53-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="50e53-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="50e53-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="50e53-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="50e53-107">O método **getchallenge** retorna um desafio do [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="50e53-107">The **GetChallenge** method returns a challenge from the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="50e53-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50e53-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="50e53-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50e53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e53-110">*lAlgoID* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="50e53-110">*lAlgoID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50e53-111">Algoritmo a ser usado no processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="50e53-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-112">*lLengthOfChallenge* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50e53-112">*lLengthOfChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e53-113">Comprimento máximo da resposta esperada.</span><span class="sxs-lookup"><span data-stu-id="50e53-113">Maximum length of expected response.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-114">*pParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50e53-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e53-115">Um objeto [**IByteBuffer**](ibytebuffer.md) que contém parâmetros específicos do fornecedor do processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="50e53-115">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="50e53-116">*pBuffer* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="50e53-116">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50e53-117">Na entrada, aponta para o buffer.</span><span class="sxs-lookup"><span data-stu-id="50e53-117">On input, points to the buffer.</span></span>

<span data-ttu-id="50e53-118">Na saída, contém os dados de desafio do cartão.</span><span class="sxs-lookup"><span data-stu-id="50e53-118">On output, contains the challenge data from the card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e53-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50e53-119">Return value</span></span>

<span data-ttu-id="50e53-120">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="50e53-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="50e53-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="50e53-121">Return code</span></span>                                                                                   | <span data-ttu-id="50e53-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="50e53-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="50e53-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="50e53-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="50e53-124">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="50e53-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="50e53-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="50e53-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="50e53-126">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="50e53-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="50e53-127"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="50e53-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="50e53-128">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="50e53-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="50e53-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="50e53-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="50e53-130">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="50e53-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="50e53-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="50e53-131">Remarks</span></span>

<span data-ttu-id="50e53-132">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="50e53-132">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="50e53-133">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="50e53-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="50e53-134">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="50e53-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50e53-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50e53-135">Requirements</span></span>



| <span data-ttu-id="50e53-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="50e53-136">Requirement</span></span> | <span data-ttu-id="50e53-137">Valor</span><span class="sxs-lookup"><span data-stu-id="50e53-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50e53-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50e53-138">Minimum supported client</span></span><br/> | <span data-ttu-id="50e53-139">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="50e53-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="50e53-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50e53-140">Minimum supported server</span></span><br/> | <span data-ttu-id="50e53-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50e53-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="50e53-142">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="50e53-142">End of client support</span></span><br/>    | <span data-ttu-id="50e53-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="50e53-143">Windows XP</span></span><br/>                                |
| <span data-ttu-id="50e53-144">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="50e53-144">End of server support</span></span><br/>    | <span data-ttu-id="50e53-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="50e53-145">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="50e53-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="50e53-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e53-147">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="50e53-147">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
